📄 **Full project report (web):**  
https://zsofia123.github.io/loan-default-prediction-ml/Predicting_Loan_Default_Using_ML_with_Regularization_Based_Model_Selection.html

# Predicting Loan Default (Credit Risk) — Leak-Free ML Pipeline

End-to-end credit risk classification project: predicting whether a loan defaults (Status: 0 = non-default, 1 = default), with a strong focus on **model validation**, **data leakage prevention**, and **cost-sensitive evaluation** (minimizing false negatives).

## Project overview
Financial institutions rely on data-driven credit scoring to make lending decisions and manage risk. In this project, I built and compared multiple models to predict loan default using borrower and loan characteristics (demographics, income, employment, credit history, LTV/DTI-related variables, etc.).

## Why this project is interesting
A key lesson was identifying and fixing **data leakage**: early results were unrealistically high for tree-based models, which triggered a validation audit. After rebuilding the pipeline so that imputation, encoding, scaling, and feature engineering are performed **train-only**, performance became realistic and comparable across models.

## Data
Source (Kaggle):


The raw dataset is **not included** in this repository. Please download it locally before running the project.

## Methodology
- Train / validation / test split: **60 / 20 / 20**
- Imbalance handling: **class-weighted learning**
- Model tuning: **cross-validation using ROC-AUC**
- Preprocessing: **leakage-free pipeline** (fit on training data only)
- Evaluation metrics: Accuracy, Precision, Recall, F1-score, ROC-AUC, Confusion Matrix
- Business focus: **minimizing false negatives** (missing true defaulters)

Models compared:
- Logistic Regression (L2, L1)
- Decision Tree
- Random Forest
- XGBoost

## Results (Leak-Free Test Set)
After removing data leakage, model performance changed materially. The best overall model on the leak-free test set was **XGBoost**, achieving the strongest balance of recall and overall discrimination.

| Model | Accuracy | Recall | F1 | ROC-AUC |
|------|----------|--------|----|---------|
| **XGBoost** | 0.87 | **0.72** | **0.73** | **0.89** |
| Random Forest | 0.88 | 0.58 | 0.71 | 0.88 |
| Decision Tree | 0.86 | 0.64 | 0.69 | 0.84 |
| Logistic Regression | 0.83 | 0.64 | 0.65 | 0.84 |

## Repository structure



## How to run
1. Clone the repository
2. Create and activate a virtual environment
3. Install dependencies


4. Download the dataset from Kaggle and place it locally.

## Notes
This project is designed as a **portfolio piece** demonstrating credit risk thinking, leakage-free model validation, and business-driven evaluation.

📄 **Full project report:**  
[Predicting Loan Default – ML with Regularization & Model Selection](reports/Predicting_Loan_Default_Using_ML_with_Regularization_Based_Model_Selection.html)

## Contact
- LinkedIn: https://www.linkedin.com/in/zsófia-kovács-434626183




