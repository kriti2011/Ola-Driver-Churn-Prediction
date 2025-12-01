# Project Objective

Ola faces high driver churn, leading to expensive re-acquisition and operational disruption.
This project builds a machine learning solution to predict whether a driver will leave the platform, enabling early retention interventions.

## 📂 Dataset Overview

Source: ola_driver.csv
Time Period: 2019–2020
Each row = One driver-month record

##  Features

Demographics	-> Age, Gender, City, Education Level

Performance Metrics-> Quarterly Rating, Total Business Value

Income & Tenure -> Monthly Income, Joining Date, Last Working Date

Role Attributes	-> Grade, Designation at Joining

Time Feature -> MMMM-YY (reporting month)

## 🔧 Project Workflow
### 1. Data Understanding & EDA

✔ Data types, structure & summary
✔ Missing value analysis
✔ Date conversion (Joining Date, LastWorkingDate, MMMM-YY)
✔ Univariate & bivariate visualizations
✔ Performance vs churn patterns
✔ Outlier & distribution assessment

### 2. Data Preprocessing

Null Value Imputation

Aggregation	Group by Driver_ID → One row per driver

Feature Engineering->	rating_increase, income_increase, tenure_days

Target Creation->	1 = churned, 0 = retained

Encoding-> One-hot encode categorical fields

Scaling-> Standardization before modeling

### 3. Modeling

Algorithms Implemented:

Bagging-> Random Forest / BaggingClassifier

Boosting -> XGBoost / LightGBM

Additional handling:
⚠ Class Imbalance → SMOTE / Class Weights

⚙ Hyperparameter Tuning → GridSearchCV

📊 Model Evaluation → Test Metrics + ROC AUC

### 📈 Evaluation Metrics

Classification Report-> Precision/Recall/F1 per class

Confusion Matrix-> Misclassification insight

ROC-AUC-> Probabilistic distinguishing power

Feature Importance-> Key churn predictors

### Deliverables visualized:

🚨 ROC-AUC Curve

🔥 Top Feature Importance Plot

📄 Model Performance Summary

### Project report - 

## 🔍 Key Insights

📉 Lower quarterly ratings strongly correlate with churn

📈 Drivers with stable or increasing income show lower attrition risk

🏙 Certain cities exhibit higher churn patterns → operational intervention

⏳ Tenure under X months → significantly higher churn probability

🟢 Incentives + support programs recommended for early-stage & low-rating drivers

## 🔥 Business Recommendations

Recommendation	                                         Impact

Targeted retention for new & low-rating drivers	         Lower acquisition costs

City-wise driver engagement programs	                   Region-specific churn reduction

Income-based incentives	                                 Improve long-term driver stickiness

Predictive churn alerts inside driver CRM	               Prevent drop-off before exit
