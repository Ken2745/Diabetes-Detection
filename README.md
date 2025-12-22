# Diabetes Risk Classification System

## Abstract
This project develops supervised machine learning models to predict the likelihood of diabetes among adults in the United States using data from the Centers for Disease Control and Prevention’s Behavioral Risk Factor Surveillance System (BRFSS). The dataset contains over 400,000 records and includes a wide range of demographic, behavioral, and physiological health indicators such as BMI, age, physical activity, smoking status, income, blood pressure, and general health condition.

The workflow begins with exploratory data analysis (EDA) to assess data quality, distributions, and class imbalance. After data cleaning and preprocessing, multiple machine learning models are trained and evaluated. Performance is measured using metrics such as AUC (micro, macro, weighted), precision, recall, F1-score, and confusion matrices.

This study highlights which features most strongly correlate with diabetes outcomes and identifies the model that best predicts diabetes likelihood. The results demonstrate how data science and machine learning can support public health analytics by improving early detection and targeted prevention strategies.

---

## Dataset Overview

- **Name:** CDC Behavioral Risk Factor Surveillance System (BRFSS)  
- **Source:** Kaggle  
  <https://www.kaggle.com/datasets/cdc/behavioral-risk-factor-surveillance-system/data?select=2015.csv>
- **Description:** Collects state-specific data on preventive health practices and risk behaviors associated with chronic diseases, injuries, and preventable infectious conditions.
- **Records:** ~400,000–500,000  
- **Data Type:** Tabular, Multivariate  
- **Target Variable:** `DIABETE3` (Diabetes Status)

### Features

- **DIABETE3** – Ever told you have diabetes  
- **_BMI5CAT** – Four categories of Body Mass Index (BMI)  
- **AGEG5YR** – Age group (5-year intervals)  
- **SEX** – Gender  
- **EXERANY2** – Exercise in the past 30 days (Physical Activity)  
- **_SMOKER3** – Computed smoking status (frequency and intensity)  
- **GENHLTH** – Self-reported general health status  
- **BPMEDS** – Currently taking medication for high blood pressure  
- **TOLDHI2** – Ever told that blood cholesterol is high  
- **CHOLCHK** – How long since last cholesterol check  
- **_RFHYPE5** – Ever told you have high blood pressure  
- **PHYSHLTH** – Number of days physical health was “not good” in the past 30 days  
- **_RFDRHV5** – Heavy alcohol consumption indicator  
---
## Models Used
✔ CatBoost Classifier
✔ Random Forest Classifier
✔ Logistic Regression (scaled features)

---

## Evaluation Metrics
- AUC (Micro, Macro, Weighted)  
- Precision  
- Recall  
- F1-Score  
- ROC-AUC  
- Confusion Matrix  
- Classification Report  

---

## Best Model

CatBoost is the top-performing model, achieving the highest micro, macro, and weighted AUC scores.

| Model                       | AUC Micro  | AUC Macro  | AUC Weighted |
| --------------------------- | ---------- | ---------- | ------------ |
| **CatBoost**                | **0.9586** | **0.7812** | **0.7715**   |
| Random Forest               | 0.8631     | 0.6049     | 0.5960       |
| Logistic Regression (SMOTE) | 0.7159     | 0.7278     | 0.6991       |

### Data Balancing Techniques

SMOTE → used for Logistic Regression

RandomOverSampler (ROS) → used for Random Forest

---

## Technologies Used

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib  
- Seaborn  
- Jupyter Notebook
- CatBoost

---
