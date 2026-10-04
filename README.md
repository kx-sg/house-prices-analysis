## Overview
A Machine Learning & Data Visualisation project predicting house sale prices (USD) using the Ames Housing Dataset. Includes exploratory data analysis, data cleaning, a Tableau dashboard, and a regression model built using scikit-learn.

## Dataset
 - **Source**: [Kaggle: House Prices - Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/data)
 - **License**: MIT
 - **Note**: The kaggle test dataset was not used because the objective was model evaluation and business insight generation rather than competition submission.

## Research Question
*Which features influence house sale prices the most?*

## Tableau Insights
 - Quality and location affect sale prices more than house size
 - Quality matters more than age, while amenities further increase value

## Tableau Dashboard
[View dashboard on Tableau Public](https://public.tableau.com/app/profile/little.pumpkin/viz/Housing_Insights_Dashboard/HousingPriceStory)

## Tools & Libraries
 - **Python:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, XGBoost, CatBoost
 - **Visualisation:** Tableau (dashboard exported to Tableau Public)

## Results (on trained dataset)
|         Model          | CV RMSE  | CV RMSE Std  |  CV MAE  | CV R squared |
|------------------------|----------|--------------|----------|--------------|
| CatBoost Tuned         | 0.1139   | 0.0110       | 0.0788   | 0.9153       |
| XGBoost Tuned          | 0.1150   | 0.0120       | 0.0790   | 0.9138       |
| CatBoost Original      | 0.1158   | 0.0102       | 0.0792   | 0.9126       |
| Ridge Tuned            | 0.1174   | 0.0100       | 0.0840   | 0.9103       |
| XGBoost Original       | 0.1200   | 0.0107       | 0.0844   | 0.9067       |
| Ridge Original         | 0.1288   | 0.0142       | 0.0893   | 0.8924       |
| Decision Tree Original | 0.1827   | 0.0186       | 0.1334   | 0.7842       |
| Baseline (Median)      | 0.3952   | 0.0236       | 0.3066   | -0.0053      |


## Results (on test dataset)
|       Model       | RMSE (log) | RMSE ($) |  MAE ($) | R squared |
|-------------------|------------|----------|----------|-----------|
| CatBoost Tuned    | 0.1194     | 19558.28 | 13578.08 | 0.9098    |


## How to Run
1. Clone this repository
2. Install dependencies: `pip install -r requirements.txt`
3. Open notebooks in order (outputs are viewable)
4. View the Tableau dashboard via the link above

## File structure
```
house-prices-analysis
├── data_files/
│   ├── cleaned_modelling_data.csv
│   ├── cleaned_tableau_data.csv
│   ├── data_description.txt
│   ├── test.csv
│   ├── train.csv
├── model_training/
│   ├── cat_results.csv
│   ├── xgb_results.csv
├── tableau/
│   ├── Housing_Insights_Dashboard.twbx
├── data_cleaning_and_eda.ipynb
├── data_cleaning_report.docx
├── house_price_analytics.pptx
├── price_regression_model.ipynb
├── README.md
├── requirements.txt
``` 

*Housing Price Analysis - ML Model & Tableau Dashboard*
*Developed by Soh Kai Xun, 2026*