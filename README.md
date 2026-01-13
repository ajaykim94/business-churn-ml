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
