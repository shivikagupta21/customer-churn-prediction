# customer-churn-prediction
Machine Learning project for telecom customer churn prediction using Random Forest, XGBoost and Decision Trees with EDA, feature importance and business recommendations.
🔍 Project Overview
This project analyzes the Telco Customer Churn dataset and applies machine learning models to predict customer churn. Churn refers to the loss of customers who stop using a company’s services, which is a critical issue for telecom companies. The objective of this project is to build predictive models, interpret churn drivers and provide actionable business recommendations to improve retention.

🎯 Objectives
1. Predict whether a customer will churn (Yes/No).
2. Identify the most important factors driving churn.
3. Compare different machine learning algorithms.
4. Provide strategic recommendations for customer retention.

📂 Dataset
Source: Telco Customer Churn Dataset (Kaggle / IBM sample dataset).
Rows: 7,043
Columns: 21 (demographic details, services, billing info, and churn status).
Target Variable: Churn (Yes/No).

🛠️ Data Preprocessing
1. Removed irrelevant column: customerID.
2. Replaced blank values in TotalCharges with 0.0 and converted to numeric.
3. Encoded categorical variables using Label Encoding.
4. Balanced target classes using SMOTE oversampling.
5. Split dataset into 80% training and 20% testing.

🤖 Machine Learning Models
The following classifiers were tested:
Decision Tree Classifier
Random Forest Classifier
XGBoost Classifier

📈 Results
Model	CV                 Accuracy	   TestAccuracy	   Precision (Churn)   	Recall (Churn)	    F1 (Churn)	  ROC-AUC
Decision Tree	             0.78	        0.77	            0.58	              0.58	            0.58	       ~0.75
Random Forest	             0.84	        0.78	            0.85	              0.85	            0.85	        0.82
XGBoost	                   0.83	        0.77	            0.80	              0.73	            0.76	       ~0.81

✅ Random Forest emerged as the best-performing model with the strongest balance of accuracy, recall, and ROC-AUC.

Key Churn Drivers (Feature Importance):
1.Contract Type
2.Monthly Charges
3.Total Charges
4.Tenure
5.Online Security & Tech Support

💡 Business Insights
1. Customers on month-to-month contracts are more likely to churn.
2. Higher monthly charges are linked with increased churn.
3. Lack of value-added services (security, tech support) contributes to attrition.
4. Customers with shorter tenure (<12 months) are at higher churn risk.

📌 Recommendations
1. Promote long-term contracts with discounts.
2. Bundle value-added services to increase stickiness.
3. Focus on early engagement for first-year customers.
4. Provide loyalty programs for high-paying customers.
5. Deploy the Random Forest model in production to flag at-risk customers.

🖥️ Tech Stack
Languages: Python
Libraries: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, XGBoost, Imbalanced-learn
Environment: Jupyter Notebook

🚀 How to Run
Clone this repository:
git clone https://github.com/your-username/customer-churn-prediction.git
cd customer-churn-prediction

Install dependencies:
pip install -r requirements.txt
Open the Jupyter notebook:
jupyter notebook Customer_Churn_Prediction_using_ML.ipynb
