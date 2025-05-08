# 📊 Customer Churn Prediction using Random Forest

This project predicts telecom customer churn using a **Random Forest Classifier**. It includes **data preprocessing**, **hyperparameter tuning using RandomizedSearchCV**, and **model evaluation**. The goal is to help telecom providers identify customers who are likely to discontinue their service.

---

## 🧠 Objective

To build a machine learning model that predicts whether a customer will churn based on their demographics, service usage, contract details, and billing information.

---

## 📁 Dataset


- **Target Variable**: `Churn` (Yes/No)
- **Features**: 
  - Demographics (gender, age, senior citizen)
  - Account info (tenure, contract type, payment method)
  - Service usage (internet service, phone service, etc.)
  - Charges (monthly charges, total charges)

---

## 📌 Steps Followed

1. **Data Preprocessing**
   - Handled missing and blank values in `TotalCharges`
   - Converted `TotalCharges` to numeric
   - Label encoded categorical variables
   - Standardized numerical features

2. **Exploratory Data Analysis**
   - Churn distribution
   - Feature-wise trends

3. **Model Training**
   - Used `RandomForestClassifier`
   - Performed hyperparameter tuning with `RandomizedSearchCV`

4. **Best Parameters Found**
   ```python
   RandomForestClassifier(
       criterion='entropy',
       max_depth=10,
       min_samples_split=5,
       n_estimators=200,
       random_state=0
   )

