# Credit Risk Prediction

## Overview

This project focuses on building a predictive model to determine the likelihood of a loan applicant defaulting on a loan. Using the Loan Prediction dataset, we performed data preprocessing, feature encoding, and implemented classification models including Logistic Regression and Decision Tree. The goal was to evaluate model performance and understand the key drivers of credit risk.

---

## Objectives

- Analyze and understand the structure of the dataset
- Handle missing values and prepare data for modeling
- Encode categorical features appropriately
- Scale features where necessary
- Train and evaluate classification models to predict loan default
- Compare model performance using accuracy and confusion matrix

---

## Dataset

The dataset used is the **Loan Prediction Dataset**, available publicly on [Kaggle](https://www.kaggle.com/). It contains records of various loan applicants and whether or not they defaulted on their loan.

---

## Tools and Libraries Used

- Python
- pandas
- numpy
- seaborn
- matplotlib
- scikit-learn

---

## Approach

1. **Data Loading**
   - Loaded the dataset using `pandas`.
   - Inspected dataset shape and verified absence of missing values.

2. **Data Preprocessing**
   - Dropped non-informative columns such as `LoanID`.
   - Encoded categorical features using `pd.get_dummies()` with `drop_first=True`.
   - Scaled numerical features using `StandardScaler` for Logistic Regression.
   
3. **Feature and Target Definition**
   - Features (`X`) were defined by excluding the target column.
   - Target (`y`) was set as the `Default` column, indicating if a loan was defaulted or not.

4. **Train-Test Split**
   - Split the data into training and testing sets using an 80/20 ratio.

5. **Model Training**
   - **Logistic Regression**: Applied to scaled feature set.
   - **Decision Tree Classifier**: Applied directly to the encoded features without scaling.

6. **Model Evaluation**
   - Used accuracy score and confusion matrix for performance evaluation.
   - Confusion matrices were visualized for better interpretability.

---

## Results

| Model              | Accuracy |
|--------------------|----------|
| Logistic Regression | 88.58%     |
| Decision Tree       | 80.27%     |

- The Decision Tree model was effective in handling both numerical and categorical data directly.
- Logistic Regression required feature scaling but also provided good performance.
- Confusion matrices helped identify misclassifications in each model.

---

## Conclusion

- Successfully built two models to predict credit default using structured loan application data.
- Logistic Regression performed well with scaled data, while Decision Tree offered ease of interpretation without the need for scaling.
- Both models highlighted key patterns that could assist financial institutions in risk assessment.
- Further enhancements can be made using cross-validation, hyperparameter tuning, and advanced ensemble methods.

---


