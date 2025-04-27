## Table of Contents
- [Project Overview](#project-overview)
- [Business Problem](#business-problem)
- [Solution Approach](#solution-approach)

# Home Credit Default Risk: Predicting Loan Repayment Outcomes

## Project Overview
Home Credit Group aims to broaden financial inclusion by providing loans to individuals who often lack traditional credit history. The challenge is accurately assessing the risk of default when conventional scoring models fall short.  
Our project uses machine learning to predict whether an applicant will repay a loan, helping Home Credit make better, faster, and fairer lending decisions.

## Business Problem
- **Objective:** Predict loan default risk for applicants with limited or unconventional financial histories.
- **Impact:**
  - Reduce financial losses from approving high-risk applicants.
  - Avoid rejecting safe borrowers, enabling responsible financial inclusion.
  - Speed up credit decision-making and automate parts of the loan process.

## Solution Approach
I developed a predictive model using structured customer data provided by Home Credit.  
Key steps included:
- **Data Cleaning:** Handled missing values through median/mode imputation. Dropped highly incomplete features (>60% missing).
- **Outlier Treatment:** Detected and capped extreme values using IQR-based Winsorization.
- **Feature Engineering:** Created meaningful features like:
  - `CREDIT_INCOME_RATIO`
  - `ANNUITY_INCOME_RATIO`
  - `EMPLOYED_TO_AGE_RATIO`
  - Groupings for age, income, and external source scores

- **Modeling:**
  - Tested Logistic Regression, Decision Tree, and Random Forest models.
  - Selected Logistic Regression due to highest AUC (0.734) and model interpretability.
  
- **Evaluation Metric:** Area Under the Curve (AUC), ideal for imbalanced datasets.

## Business Value
- Supports Home Credit's mission of expanding financial access to underserved customers.
- Reduces risk by improving default predictions.
- Enables faster and more consistent loan decision-making.

## Key Learning
- Importance of careful feature engineering when working with real-world data.
- The trade-off between model complexity and interpretability for business applications.
- Handling imbalanced datasets using appropriate evaluation metrics.
