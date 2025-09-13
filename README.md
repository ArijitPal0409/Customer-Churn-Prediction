# Customer-Churn-Prediction
Project Overview

Customer churn is a critical problem in the telecom industry, where retaining existing customers is often more cost-effective than acquiring new ones. This project builds machine learning models to predict whether a customer is likely to churn, based on demographic, contract, and billing information.

The goal is not only to predict churn but also to identify key drivers of churn that can help businesses design effective retention strategies.

# Dataset
Source : https://www.kaggle.com/datasets/maqeel732/wa-fn-usec-telco-customer-churn-csv
Size:  ~7,000 customer records

Features:

Customer demographics (gender, senior citizen, dependents)
Services subscribed (Internet, OnlineSecurity, TechSupport, Streaming)
Contract details (tenure, contract type, payment method)
Billing details (monthly charges, total charges)
Target: Churn (Yes = 1, No = 0)

# Project Workflow

Data Preprocessing
  Handled missing values
  Encoded categorical variables
  Scaled numeric features
  Train-test split (80/20)
Modeling
  Logistic Regression
  Random Forest
  XGBoost
Evaluation Metrics
  Accuracy, Precision, Recall, F1-Score
  ROC-AUC Score
  Feature Importance Analysis

# Results

Model	      Accuracy	      Recall(Churn=1)    	ROC-AUC

Logistic 
Regression	 0.80	              0.55	           0.84

Random 
Forest	     0.79	              0.50             0.82

XGBoost	     0.78     	        0.52	           0.82


Key Insight:

Logistic Regression gave the best balance with 84% ROC-AUC and higher recall (55%), making it the most effective for churn detection.

Customers with short tenure, high monthly charges, and month-to-month contracts are most likely to churn.

Services like OnlineSecurity and TechSupport reduce churn risk.

Feature Importance (Random Forest Example)

Top 5 churn drivers:
 -Contract Type
 -Tenure
 -Monthly Charges
 -Total Charges
 -Online Security
 ![Feature Importance](feature_importance.png)

Tech Stack
Language: Python
Libraries: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, XGBoost
Platform: Google Colab

#How to Run

Clone this repo / open in Google Colab
Mount Google Drive & load dataset
Run all cells in Customer_Churn_Prediction.ipynb
View evaluation metrics & feature importance

#Future Improvements

Hyperparameter tuning with GridSearchCV
Deploy model using Flask/Streamlit
Build an interactive dashboard (Tableau/Power BI) for churn insights

#Author
Linked ln : www.linkedin.com/in/arijit-pal-1a4b55211
