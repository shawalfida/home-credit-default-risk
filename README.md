# Home Credit Default Risk: Predicting Loan Repayment Outcomes

## 📋 Table of Contents
- [Project Overview](#project-overview)
- [Business Problem](#business-problem)
- [Solution Approach](#solution-approach)
- [My Contribution](#my-contribution)
- [Business Value of Solution](#business-value-of-solution)
- [Challenges Faced](#challenges-faced)
- [Key Learnings](#key-learnings)

---

## Project Overview
Home Credit Group aims to expand financial inclusion by providing loans to individuals who often lack traditional credit histories. The project focuses on predicting the likelihood that a loan applicant will repay their loan, helping Home Credit make better, faster, and fairer lending decisions.

---

## Business Problem
**Objective:**  
Predict loan default risk for applicants with limited or unconventional financial histories.

**Impact if solved:**  
- Reduce financial losses from approving high-risk applicants.
- Avoid rejecting creditworthy customers, promoting responsible financial inclusion.
- Speed up and automate parts of the loan approval process.

---

## Solution Approach
I developed a predictive model using structured customer data provided by Home Credit.  
Key steps included:

- **Data Cleaning:**  
  - Dropped highly incomplete features (>60% missing).
  - Imputed missing values using median (numerical) and mode (categorical).

- **Outlier Treatment:**  
  - Detected extreme values (e.g., unrealistic income or children counts) and capped them using IQR-based Winsorization.

- **Feature Engineering:**  
  - Created new features like:
    - `CREDIT_INCOME_RATIO`
    - `ANNUITY_INCOME_RATIO`
    - `EMPLOYED_TO_AGE_RATIO`
    - Grouped variables for age, income, and external source scores.

- **Modeling:**  
  - Tested Logistic Regression, Decision Tree, and Random Forest.
  - Selected **Logistic Regression** based on best performance (highest AUC = 0.734) and strong interpretability.

- **Evaluation Metric:**  
  - Used **AUC (Area Under the Curve)**, which is ideal for evaluating imbalanced classification problems.

---

## My Contribution
- Independently performed data cleaning, feature engineering, and model evaluation.
- Led decisions on feature selection and model comparison.
- Focused on balancing predictive power with the business need for model transparency.

---

## Business Value of Solution
- Helps Home Credit serve a broader base of underserved customers.
- Improves credit decision-making accuracy, reducing financial losses.
- Promotes faster, more consistent lending operations.

---

## Challenges Faced
- **Severe Class Imbalance:** Only about 8% of applicants defaulted. Solved by using AUC instead of raw accuracy.
- **Missing Data:** Some variables had >60% missing values, requiring careful dropping or imputation.
- **Bias from External Scores:** Needed to balance predictive power with fairness and Home Credit’s inclusion goals.

---

## Key Learnings
- Importance of designing transparent models when financial inclusion is a goal.
- Trade-off between model complexity and business interpretability.
- Best practices for handling real-world issues like missing values, outliers, and imbalanced classes.

---