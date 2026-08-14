# Assignment 2 — Diabetes Prediction using Machine Learning

End-to-end binary classification pipeline (Pima Indians Diabetes dataset) using Pandas, NumPy, Matplotlib, Seaborn, and Scikit-learn.

## Files

- `Diabetes_Prediction_ML.ipynb` — the analysis & modeling notebook (Colab-ready; loads from `/content/diabetes.csv`).
- `UST_Assignment2_Diabetes_Report.pdf` — documentation report (data prep, model building, training, evaluation, performance analysis).
- `diabetes.csv` — the dataset (768 patient records, 8 features + target).
- `charts/` — exported visualizations.

## How to run

1. Open `Diabetes_Prediction_ML.ipynb` in Google Colab.
2. Upload `diabetes.csv` to the session (it will sit at `/content/`).
3. Runtime → Run all.

## Key findings

- 768 records; hidden missing values (encoded as 0) in Glucose, BloodPressure, SkinThickness, Insulin and BMI were imputed with the median.
- Three models compared: Logistic Regression, Decision Tree, Random Forest.
- **Decision Tree** performed best on the test set (Accuracy ~76%, Recall ~72%, F1 ~0.68).
- Random Forest showed the largest train/test gap (mild overfitting); Logistic Regression was the most consistent but had the lowest Recall.
- **Recall** is the most important metric for this problem — missing an actual diabetes case (False Negative) is more costly than a false alarm.
- Glucose is by far the strongest predictor, followed by BMI and Age.
- Recommended improvements: handle class imbalance (SMOTE / class weighting) and hyperparameter tuning.
