# Diabetes Prediction Using Logistic Regression

## Project Overview
This project uses Logistic Regression to predict a binary diabetes-related outcome from health indicators in the BRFSS 2015 dataset.

The original `Diabetes_012` target has three classes:
- `0`: No diabetes
- `1`: Prediabetes
- `2`: Diabetes

For this project, classes `1` and `2` are combined into one positive class.

## Student Details
- **Name:** Anushka Kiran Gundale
- **Project:** Diabetes Prediction Using Health Indicators

## Dataset
The project uses the BRFSS 2015 Diabetes Health Indicators dataset.

- Original dataset size: 253,680 rows and 22 columns
- Input features used: 21
- Training samples: 183,824
- Testing samples: 45,957

## Methodology
1. Load and inspect the dataset.
2. Remove duplicate rows.
3. Convert the target into a binary classification problem.
4. Split the data into training and testing sets.
5. Scale the features using `StandardScaler`.
6. Train Logistic Regression with balanced class weights.
7. Evaluate the model using classification metrics and a confusion matrix.
8. Interpret the model coefficients.

## Model
- **Algorithm:** Logistic Regression
- **Feature scaling:** StandardScaler
- **Class weighting:** Balanced
- **Maximum iterations:** 1000

## Results

| Metric | Score |
|---|---:|
| Accuracy | 0.7195 |
| Precision | 0.3532 |
| Recall | 0.7489 |
| F1-score | 0.4800 |
| ROC-AUC | 0.8053 |

### Confusion Matrix

|  | Predicted 0 | Predicted 1 |
|---|---:|---:|
| Actual 0 | 27,115 | 10,897 |
| Actual 1 | 1,995 | 5,950 |

## Key Findings
The model achieved a ROC-AUC of 0.8053 and detected approximately 74.9% of positive cases. Recall was relatively high, but precision was lower, indicating that some negative cases were incorrectly predicted as positive.

The largest positive coefficients reported in the notebook were:
- General Health: 0.5504
- BMI: 0.4660
- Age: 0.4493
- High Blood Pressure: 0.3278

## Files
- `Project3.ipynb` — Python notebook containing the project workflow and results
- `Diabetes_Logistic_Regression_Report_Anushka_Gundale.docx` — project report

## Limitation
This project is for educational purposes only and must not be used for medical diagnosis. The assignment handout specifies the Pima Indians Diabetes dataset, while this project uses BRFSS 2015. Confirm that the dataset substitution is acceptable before submission.
