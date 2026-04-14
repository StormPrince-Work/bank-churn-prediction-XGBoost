# 📊 Customer Churn Prediction (Kaggle Project)
## 📌 Overview
This project focuses on predicting customer churn for a bank using machine learning techniques (XGBoost). The goal is to identify customers who are likely to leave, with the potential for enabling businesses to take proactive retention measures.
The project includes full data preprocessing, exploratory data analysis (EDA), feature engineering (binning and additional features), and model development. Further I used Optuna to optimise hyperparameter selection. 
Kaggle Competition link: https://www.kaggle.com/competitions/playground-series-s4e1/data
## 📂 Dataset
- Source: Kaggle (Churn Modelling Dataset)
- Features include:
  - Demographics (Age, Gender, Geography)
  - Account information (Balance, Tenure, NumOfProducts)
  - Activity indicators (IsActiveMember, HasCrCard)
- Target variable:
  - `Exited` (1 = Churned, 0 = Retained)
## 🔍 Exploratory Data Analysis
Key insights from EDA:
- Active members are significantly less likely to churn
- Customers with 3+ products show unusual churn behavior
- Geography plays a strong role in churn rates
- Tenure shows non-linear relationships with churn
- Binning age enabled the model to represent customers over 70 years old.
Visualisations were created using Plotly, Matplotlib and Seaborn to compare churn vs retained customers across multiple features.

## ⚙️ Feature Engineering
- Combined train/test datasets for consistent preprocessing
- Handled categorical variables (One Hot encoding and Label Encoding)
- Created binned features and created features comparing against a baseline.
- Cleaned and standardized numerical features.

## 🤖 Models Used
- Logistic Regression
- XGBoost

## Results 
- Best Model: XGBoost with Optuna, with Age Binning and encoding.
- Kaggle Competition Scores on TestSet: Private: 0.8061, Public: 0.80536
