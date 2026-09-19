# Credit-Score-Classification
Credit Score Classification using Machine Learning for Financial Risk Assessment


A machine learning project to classify customers into **Poor, Standard, and Good credit score categories** using financial and credit-related attributes.

## Project Objective

The objective of this project is to build a classification model that can support credit score assessment using customer financial and credit history data.

The project focuses on data cleaning, exploratory analysis, model comparison, and identifying important factors influencing credit score classification.

## Dataset

- Training data: **100,000 rows × 28 columns**
- Test data: **50,000 rows × 27 columns**
- Target variable: `Credit_Score`
- Classes: **Poor, Standard, Good**

The dataset contains financial, credit history, payment behaviour, and personal attributes.

## Data Cleaning & Preprocessing

The dataset contained inconsistent data types, missing values, invalid placeholder values, and multi-value text fields.

Key preprocessing steps included:

- Replaced invalid placeholder values with missing values
- Converted numeric fields stored as text into numeric format
- Converted credit history age into months
- Created `Loan_Count` from loan information
- Handled unrealistic age values
- Removed identifier, PII, and redundant columns
- Applied preprocessing through a machine learning pipeline

## Exploratory Data Analysis

EDA was performed to understand the target distribution and relationships between important financial features.

Key observations included relationships between:

- Outstanding debt and credit history
- Outstanding debt and loan count
- Payment delays and outstanding debt
- Credit history and repayment behaviour

## Models Used

The following classification models were compared:

- Logistic Regression
- Random Forest
- XGBoost

### Model Performance

| Model | Accuracy | Balanced Accuracy | F1 Score |
|---|---:|---:|---:|
| Random Forest | 78.3% | 76.6% | 76.8% |
| XGBoost | 75.9% | 72.2% | 72.4% |
| Logistic Regression | 61.4% | 57.1% | 57.6% |

**Random Forest performed best among the tested models.**

## Feature Importance

Important features identified by the Random Forest model included:

- Outstanding Debt
- Interest Rate
- Delay from Due Date
- Changed Credit Limit
- Credit History Age
- Annual Income
- Credit Utilization Ratio

## Key Findings

- Random Forest achieved the strongest performance among the tested models.
- Debt-related and payment-related features were important signals for credit score classification.
- Some classification errors occurred between neighbouring credit score categories, particularly Poor vs Standard and Standard vs Good.
- The project demonstrates how machine learning can support more consistent and data-driven credit risk assessment.

## Tools & Technologies

**Python | Pandas | NumPy | Matplotlib | Seaborn | Plotly | Scikit-learn | XGBoost | Jupyter Notebook**

## Project File

- `credit_score_classification_project_Yogita.ipynb` — Complete data analysis, preprocessing, model training, evaluation, and prediction workflow.
