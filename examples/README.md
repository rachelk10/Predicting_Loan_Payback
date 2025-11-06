# Exploratory Data Analysis Examples

This folder contains sample visualizations and analysis from the project.

## Feature Importance

The most important features identified by the LightGBM model:
- Credit score
- Interest rate  
- Debt-to-income ratio
- Engineered features (loan-to-income ratio, risk score)

## Target Distribution

The dataset shows a balanced distribution between:
- Loans paid back (class 1)
- Loans not paid back (class 0)

This balance allows for effective model training without requiring special sampling techniques.

## Correlation Analysis

Key findings from correlation analysis:
- Strong negative correlation between credit score and default rate
- Interest rate highly correlated with loan risk
- Debt-to-income ratio is a significant predictor

For full EDA with visualizations, refer to the original exploration notebook.
