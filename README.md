# Loan Default Risk Prediction

This project aims to implement multiple Logistic Regression models to accurately predict loans at risk of default.

## Project Summary

Financial institutions face the challenge of distinguishing between loans likely to be paid off and those at risk of default. This project develops a predictive model to effectively separate risky loans from secure ones.

We utilize a dataset with 77,500 entries and 7 features including loan size, interest rates, borrower's income, debt-to-income ratios, account numbers, derogatory incidents, and total debt. These features forecast the loan's outcome, which may be secure or at risk.

The primary hurdle in loan outcome prediction is the imbalanced nature of the dataset, with 96.8% of loans being secure and only 3.2% at risk. A simple accuracy-focused model could overlook vital at-risk loans.

### Data Processing Workflow

- Load a CSV dataset into a pandas DataFrame.
- Perform preliminary data analysis.
- Divide the 7 features and the target variable, "loan outcome," into separate DataFrames.
- Split these DataFrames into training and testing subsets with stratification to address the imbalanced data.
- Employ StandardScaler to normalize the datasets for training and testing.

### Model Evaluation

We assessed two Logistic Regression models:

1. **Model 1**: Trained on normalized data with stratification to reflect the imbalanced dataset.
2. **Model 2**: Trained on data augmented via random oversampling to achieve a balanced dataset for a fair comparison of loan outcomes.

The models were evaluated based on their ability to identify at-risk loans without sacrificing the prediction accuracy for secure loans.
