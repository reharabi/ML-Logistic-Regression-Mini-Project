# 💼 Income Classification with Logistic Regression

This project builds a logistic regression model to predict whether an individual's income exceeds $50K/year based on demographic and employment data. It includes thorough preprocessing, feature engineering, and model evaluation.

> 🏫 This project was developed as part of Masterschool's mini project on Machine Learning, focusing on income classification using logistic regression

---

## 📦 Dataset

- Source: [UCI Adult Income Dataset](https://archive.ics.uci.edu/ml/datasets/adult)
- Format: CSV
- Target: `income` (binary: `<=50K` or `>50K`)

---

## 🔧 Workflow Overview

### 1. Preprocessing
- Replaced `" ?"` with `NaN` and imputed missing categorical values using mode
- Capped outliers using IQR method
- Transformed skewed features (`capital-gain`, `capital-loss`) with log transformation

### 2. Feature Engineering
- Created `is_married_and_working`: flags married individuals working in private/self-employed sectors
- Created `has_advanced_education`: flags individuals with Bachelors, Masters, Doctorate, or Prof-school degrees

### 3. Feature Scaling
- Compared Min-Max Scaling and Z-score Standardization
- Chose Z-score for consistency across varied ranges

### 4. Encoding Categorical Variables
- Used both `get_dummies()` and `OneHotEncoder`
- Preferred `OneHotEncoder` for production due to pipeline compatibility and memory efficiency

### 5. Model Training
- Used Logistic Regression with `max_iter=5000`
- Train-test split: 80/20 with stratification

### 6. Evaluation
- Accuracy: **83.91%**
- Sample predictions vs actuals displayed
- Reflected on limitations of accuracy in imbalanced datasets

---

## 📊 Key Takeaways

- **Accuracy alone is not enough**: imbalance in income classes can mislead performance metrics
- **Feature engineering matters**: marital status and education level improved model interpretability
- **Z-score scaling** is ideal for datasets with mixed numeric ranges
- **OneHotEncoder** is preferred for scalable, production-ready pipelines

---

## 📁 Files

- [income_model.ipynb](https://github.com/reharabi/ML-Logistic-Regression-Mini-Project/blob/main/Logistic_Regression_Adult_Income_Dataset%20(2).ipynb) – Main notebook  
- [`adult.data`](https://archive.ics.uci.edu/ml/datasets/adult) – Raw dataset

---

## 🛠 Tools Used

- Python (pandas, numpy, seaborn, matplotlib)
- Scikit-learn (LogisticRegression, preprocessing, metrics, accuracy_score)

---

Created by Reha Rabi 
For questions or collaboration, feel free to connect via GitHub or LinkedIn.

