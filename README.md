
# Customer Churn Prediction & Business Intelligence

## 📌 Project Overview

This project develops an end-to-end **Customer Churn Prediction system** for a telecommunications business.

The objective is to identify customers who are likely to churn and understand the factors associated with customer churn so that businesses can take proactive customer-retention actions.

The project combines:

- Exploratory Data Analysis
- Statistical Analysis
- Business-driven Feature Engineering
- Machine Learning
- Model Evaluation
- Model Optimization
- Explainable AI using SHAP
- Business Interpretation

---

## 🎯 Problem Statement

Customer churn is a major business challenge for telecommunications companies because losing existing customers can negatively affect recurring revenue and customer lifetime value.

The goal of this project is to:

1. Understand customer churn patterns.
2. Identify variables associated with churn.
3. Build machine learning models to predict churn.
4. Compare different classification algorithms.
5. Optimize the model for better identification of potential churners.
6. Explain model predictions using SHAP.
7. Translate analytical findings into actionable business recommendations.

---

## 📊 Dataset

The project uses the **IBM Telco Customer Churn dataset**.

The original dataset contains approximately 7,000 customer records and includes information related to:

- Customer demographics
- Tenure
- Phone services
- Internet services
- Online security
- Technical support
- Streaming services
- Contract type
- Payment method
- Monthly charges
- Total charges
- Churn status

### Dataset Link

https://www.kaggle.com/datasets/blastchar/telco-customer-churn

---

## 🔄 Project Workflow

### Phase 1–2: Problem & Data Understanding

Defined the telecom customer churn problem and examined the structure, variables and business context of the dataset.

### Phase 3: Data Cleaning

Performed:

- Duplicate detection and removal
- Missing-value analysis
- Data-type correction
- Numerical conversion
- Target-variable encoding

After cleaning, the dataset contained **7,021 customer records**.

### Phase 4: Exploratory Data Analysis

Performed EDA to understand:

- Churn distribution
- Numerical variable distributions
- Customer tenure
- Monthly and total charges
- Contract type
- Internet service
- Payment methods
- Customer service usage

The overall churn rate was approximately **26.45%**.

### Phase 5: Statistical Analysis

Statistical methods were used to validate relationships observed during EDA.

Methods included:

- Chi-square tests for categorical variables
- Independent-samples t-tests
- Correlation analysis

A significance level of **α = 0.05** was used.

The analysis helped distinguish statistically significant relationships from relationships that were not supported by sufficient statistical evidence.

### Phase 6: Feature Engineering

Created **26 business-driven features** from the original customer variables.

Examples include:

- `TenureGroup`
- `IsNewCustomer`
- `LongTermCustomer`
- `CustomerAgeScore`
- `ServiceCount`
- `EntertainmentServices`
- `SecurityServices`
- `PremiumUser`
- `MultiServiceUser`
- `ChargeCategory`
- `RevenueSegment`
- `AvgChargePerMonth`
- `HighMonthlyCharge`
- `FamilyCustomer`
- `IndependentCustomer`
- `LongTermContract`
- `AutoPayment`
- `ElectronicPayment`
- `PaperlessCustomer`
- `InternetUser`
- `FiberCustomer`
- `InternetAddOnCount`
- `CustomerValueScore`
- `LoyaltyScore`
- `HighRiskCustomer`

The feature-engineered dataset contains **7,021 records and 46 columns**.

### Phase 7–8: Machine Learning

Built and compared multiple classification algorithms:

- Logistic Regression
- Decision Tree
- Random Forest
- LightGBM
- XGBoost

Models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

### Model Performance

| Model | Accuracy | Precision | Recall | F1 | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 80.78% | 67.96% | 51.88% | 58.84% | 84.16% |
| Decision Tree | 78.79% | 64.68% | 43.82% | 52.24% | 82.05% |
| Random Forest | 79.50% | 65.33% | 48.12% | 55.42% | 83.82% |
| LightGBM | 78.29% | 61.20% | 49.19% | 54.55% | 82.98% |
| XGBoost | 77.79% | 60.20% | 47.58% | 53.15% | 83.02% |

Logistic Regression provided the strongest baseline ROC-AUC among the evaluated models.

### Phase 9: Threshold Optimization

The classification threshold was optimized to improve the identification of potential churners.

The optimized model achieved approximately:

- Recall: **74%**
- Precision: **53%**
- F1-score: **62%**
- Accuracy: **76%**

The optimization prioritizes identifying more potential churners, which can be useful when the business wants to proactively target customers for retention.

### Phase 10: Explainable AI

SHAP (SHapley Additive exPlanations) was used to understand model predictions.

The analysis included:

- SHAP summary plots
- Feature importance
- Dependence plots
- Individual customer explanations
- Waterfall/force explanations

Important predictive factors included variables related to:

- Tenure
- Average charges
- Service usage
- Internet service
- Contract type
- Customer support/security services

SHAP helped connect machine learning predictions with interpretable business insights.

---

## 💼 Business Insights

The analysis indicates that customer churn is associated with several customer characteristics, including:

- Customer tenure
- Contract type
- Monthly charges
- Internet service
- Payment method
- Service and support usage

These findings can support targeted retention strategies such as:

- Early-stage customer engagement
- Targeted retention offers
- Contract-based incentives
- Improved technical support
- Security/service bundles
- Personalized customer interventions

The project focuses on **predictive associations rather than causal claims**.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- LightGBM
- XGBoost
- SHAP
- Statistical Analysis
- Google Colab

---

## 📁 Project Structure

```text
Customer-Churn-Prediction/
│
├── README.md
│
├── notebooks/
│   ├── 01_Data_Cleaning.ipynb
│   ├── 02_EDA.ipynb
│   ├── 03_Statistical_Analysis.ipynb
│   ├── 04_Feature_Engineering.ipynb
│   └── 05_Feature_Selection_Machine_Learning.ipynb
│
├── results/
│
├── visuals/
│
└── requirements.txt
