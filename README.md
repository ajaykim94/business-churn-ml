# Customer Churn Prediction – Business-Focused Machine Learning

## Overview
Customer churn is a major revenue risk for subscription-based businesses. Retaining existing customers is often significantly cheaper than acquiring new ones.

This project builds an end-to-end machine learning pipeline to:
1. Predict which customers are likely to churn
2. Identify the key drivers of churn
3. Translate model outputs into actionable business decisions

The emphasis is not only on model performance, but on **interpretability and decision-making**.

---

## Business Problem
Given historical customer data, can we identify customers at high risk of churn and recommend targeted retention strategies that balance cost and effectiveness?

---

## Dataset
- **Source:** IBM Telco Customer Churn dataset
- **Size:** ~7,000 customers
- **Target:** Binary churn indicator
- **Features:** Customer demographics, subscription details, tenure, and billing information

---

## Project Structure
- `01_eda.ipynb` – Exploratory Data Analysis and business insights
- `02_feature_engineering.ipynb` – Feature creation and preprocessing
- `03_modeling.ipynb` – Baseline and advanced ML models
- `04_evaluation_and_decisions.ipynb` – Threshold tuning and business trade-offs

---

## Models Used
- Logistic Regression (baseline)
- Random Forest
- Gradient Boosting / XGBoost

---

## Evaluation Metrics
- ROC-AUC
- Precision / Recall
- F1-score
- Confusion matrix at multiple thresholds

---

## Results

The final XGBoost model achieved:
- ROC-AUC: 0.83
- PR-AUC: 0.64

These results indicate strong ranking performance on an imbalanced churn dataset,
enabling effective prioritization of high-risk customers.

## Key Drivers of Churn (SHAP Analysis)

SHAP feature attribution shows that churn risk is primarily driven by:

- High monthly charges relative to tenure, indicating poor perceived value early in the customer lifecycle
- Month-to-month contract status, reflecting low switching costs
- Short customer tenure, particularly within the first year
- Lack of online security and technical support services
- Higher overall billing amounts combined with low contractual commitment

These results align with known churn dynamics in subscription businesses and provide
clear levers for targeted retention strategies.


## Business Impact
By tuning the decision threshold, the model can target approximately 25–30% of customers
while capturing over 75% of churn risk, allowing retention teams to focus incentives
where they are most cost-effective.


## Key Business Insights
- Customers on month-to-month contracts exhibit significantly higher churn rates
- Low-tenure customers with high monthly charges are at greatest risk
- Proper threshold selection enables targeting a minority of customers while capturing the majority of churners

---

## Recommendations
- Prioritize retention efforts for customers with tenure < 12 months
- Offer incentives selectively to customers with high predicted churn risk
- Deploy the model as a recurring churn scoring tool for customer success teams

---

## Technologies
Python, Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, Seaborn

---

## Author
Augustin Kim  
UC Berkeley – Master of Information and Data Science
