# PowerCo SME Customer Churn Prediction

This repository contains a data science project developed for PowerCo, a major utility provider, as part of a BCG strategy simulation. The goal is to analyze customer churn within the SME (Small and Medium Enterprise) segment and build a predictive model to identify at-risk customers.

# 📌 Project Overview

PowerCo is experiencing a customer churn rate of 9.7%. Our task was to investigate the drivers of this churn—specifically the impact of price sensitivity—and provide a data-driven solution to improve customer retention.

# 🛠️ Data Science Workflow

## 1. Data Cleaning & EDA
- Handled missing data and outliers in consumption and price datasets.
- Log-transformed highly skewed consumption data to improve model stability.
- Discovered that churners are distributed across various price points, suggesting price sensitivity isn't the only factor.

## 2. Feature Engineering
- **Price Volatility:** Calculated the difference between December and January prices to measure sensitivity to year-end changes.
- **Usage Metrics:** Created features for average consumption, net margin, and contract tenure.
- **Categorical Encoding:** Processed sales channels and geographic origins for machine learning readiness.

## 3. Machine Learning Modeling
- **Model:** Random Forest Classifier (1000 trees)
- **Performance:**
  - Accuracy: 90.36%
  - Precision: 85.00%
  - Recall: 4.64% (indicates a need for further optimization on identifying all churners)
- **Top Features:** Annual consumption (`cons_12m`), net margin, and forecasted meter rent were identified as the strongest predictors.

# 💼 Business Recommendations
- **Targeted Intervention:** Use the model to identify high-probability churners and offer a 20% discount incentive.
- **Proactive Retention:** Focus on high-margin customers with decreasing consumption patterns, as they represent the highest revenue risk.
- **Model Refinement:** Incorporate more behavioral data (customer service calls, portal logins) to improve the detection rate of at-risk customers.
