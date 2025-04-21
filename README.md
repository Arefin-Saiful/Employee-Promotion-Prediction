# 🏢 Employee Promotion Prediction – ML2 Project

This project leverages machine learning to predict employee promotion eligibility using HR data. The goal is to build a classification model that assists companies in making fair, data-driven promotion decisions based on historical employee performance and demographics.

---

## 📊 Problem Statement

Promotion decisions often involve reviewing large volumes of employee data, which can lead to delays, bias, or missed opportunities. Using machine learning, we aim to automate this process for **JMD Company** by predicting whether an employee should be promoted based on their:

- Training score
- Past performance rating
- Awards
- Education
- Tenure and other attributes

---

## 🧾 Dataset Overview

- **Rows:** 54,808  
- **Columns:** 14  
- **Target Variable:** `is_promoted` (1 = promoted, 0 = not promoted)  
- **Class Imbalance:** ~91.5% not promoted vs. ~8.5% promoted  

### Features include:
- `department`, `region`, `education`, `gender`, `recruitment_channel`
- `no_of_trainings`, `age`, `previous_year_rating`, `length_of_service`
- `awards_won`, `avg_training_score`

---

## 🔎 Exploratory Data Analysis (EDA)

The EDA uncovered:
- High correlation between `avg_training_score`, `awards_won`, and promotion
- Strong influence of `previous_year_rating` and `length_of_service`
- Imbalance in class distribution and several outliers in numerical features

---

## 🛠️ Preprocessing

- Missing values handled using mode, median, and mean
- Outliers removed via IQR method
- Label encoding for categorical variables
- Feature scaling using standardization
- Feature engineering (e.g., training efficiency)

---

## 🤖 Model Building

### Models Used:
- Decision Tree
- Random Forest
- Bagging
- AdaBoost
- Gradient Boosting
- XGBoost

### Techniques Applied:
- SMOTE Oversampling
- Random Undersampling
- Hyperparameter tuning
- Stratified Train/Validation/Test Split

---

## 🏆 Final Model

The **Gradient Boosting Classifier (original data)** was selected based on balanced performance across training and validation:

| Metric     | Value  |
|------------|--------|
| Accuracy   | 0.975  |
| Recall     | 0.914  |
| Precision  | 0.931  |
| F1-Score   | 0.922  |

---

## 🔍 Feature Importance

Top predictors of promotion:
1. Average Training Score
2. Length of Service
3. Previous Year Rating
4. Awards Won
5. Number of Trainings

---

## ✅ Key Takeaways

- **Awards** and **training scores** are strong indicators of promotion
- **Gradient Boosting** is the most robust model across techniques
- **Class imbalance** was successfully handled via SMOTE

---

## 📌 Recommendations

- Invest in structured training programs
- Improve employee retention strategies
- Reward high-performing employees consistently
- Use dashboards to visualize promotion readiness
- Address any promotion process gaps or biases

---
