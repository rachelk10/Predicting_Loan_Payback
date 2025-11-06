# Loan Payback Prediction - Kaggle Competition

A machine learning solution for predicting loan repayment probability using ensemble methods (LightGBM + XGBoost).

## 📊 Project Overview

This project tackles the binary classification problem of predicting whether a borrower will pay back their loan based on various financial and demographic features.

- **Competition**: Kaggle Playground Series S5E11
- **Evaluation Metric**: ROC AUC Score
- **Target Variable**: `loan_paid_back` (1 = paid back, 0 = default)

## 🎯 Model Performance

- **LightGBM**: ROC AUC ~0.XXX
- **XGBoost**: ROC AUC ~0.XXX
- **Ensemble**: ROC AUC ~0.XXX (Average of both models)

## 🚀 Key Features

### Feature Engineering
Created 12 engineered features to improve model performance:
- Financial ratios (loan-to-income, payment-to-income, debt-to-income)
- Monthly payment estimation
- Credit score categories (Poor, Fair, Good, Very Good, Excellent)
- Income and interest rate categories
- Risk score (custom composite metric)
- Interaction features (income × credit score)

### Models Used
- **LightGBM**: Gradient boosting with optimized hyperparameters
- **XGBoost**: Extreme gradient boosting for robust predictions
- **Ensemble**: Average of both models for improved stability

### Data Preprocessing
- Label encoding for categorical variables
- Standard scaling for numerical features
- Stratified train-validation split (80/20)
- Missing value imputation

## 📁 Project Structure

```
├── kaggle_minimal.ipynb    # Main notebook with production code
├── README.md               # Project documentation
├── requirements.txt        # Python dependencies
└── submission.csv          # Kaggle submission file (generated)
```

## 🛠️ Installation & Usage

### Prerequisites
```bash
pip install -r requirements.txt
```

### Running the Notebook
1. Download the dataset from [Kaggle Competition](https://www.kaggle.com/competitions/playground-series-s5e11)
2. Update the data paths in the notebook
3. Run all cells sequentially
4. The submission file will be generated as `submission.csv`

### Quick Start
```python
# The notebook follows this workflow:
1. Load data
2. Engineer features
3. Preprocess and encode
4. Train models with cross-validation
5. Create ensemble predictions
6. Generate submission file
```

## 📈 Methodology

1. **Exploratory Data Analysis**: Understanding feature distributions and correlations
2. **Feature Engineering**: Creating meaningful financial indicators
3. **Model Training**: Using gradient boosting algorithms with early stopping
4. **Validation**: Stratified split to maintain class balance
5. **Ensemble**: Combining predictions for better generalization

## 🔧 Hyperparameters

### LightGBM
- Learning rate: 0.05
- Num leaves: 31
- Max depth: -1 (no limit)
- Feature/Bagging fraction: 0.8
- Regularization: L1=0.1, L2=0.1

### XGBoost
- Learning rate: 0.05
- Max depth: 6
- Subsample: 0.8
- Column sample: 0.8
- Regularization: L1=0.1, L2=1.0

## 🎓 Key Insights

- **Most Important Features**: Credit score, interest rate, debt-to-income ratio, and engineered financial ratios
- **Model Choice**: Ensemble method outperforms individual models
- **Feature Engineering Impact**: Custom features significantly improve prediction accuracy

## 🔄 Potential Improvements

- [ ] Hyperparameter tuning with Optuna or GridSearchCV
- [ ] Add CatBoost to the ensemble
- [ ] Implement stacking instead of simple averaging
- [ ] Cross-validation with K-folds for more robust evaluation
- [ ] Feature selection to reduce dimensionality
- [ ] Handle outliers with robust scaling methods

## 📝 License

This project is open source and available under the MIT License.

## 👤 Author

Rachel Shor - [GitHub Profile](https://github.com/rachelk10)

## 🙏 Acknowledgments

- Kaggle for hosting the competition
- The open-source community for LightGBM and XGBoost libraries
