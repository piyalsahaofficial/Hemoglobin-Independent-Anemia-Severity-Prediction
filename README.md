# Hemoglobin-Independent Anemia Severity Prediction

A machine learning project for predicting anemia severity **without using Hemoglobin (Hb) as an input feature**. The project compares Random Forest, XGBoost, and LightGBM, with SHAP used for model explainability.

---

## Project Overview

The project predicts four anemia severity classes:

- Normal
- Mild
- Moderate
- Severe

Severity labels are created using clinically grounded thresholds based on WHO 2024 criteria, considering age and gender.

---

## Models

Three tree-based machine learning models are compared:

- Random Forest
- XGBoost
- LightGBM

Model evaluation uses **stratified 5-fold cross-validation**.

---

## Features

Hb is excluded from the prediction features.

The models use demographic and hematological features including:

Gender, Age, RBC, WBC, PLATELETS, LYMP, MONO, HCT, MCV, MCH, MCHC, RDW, PDW, MPV, PCT

---

## Evaluation & Explainability

The project includes:

- Accuracy
- Macro Precision
- Macro Recall
- Macro F1-score
- Confusion Matrices
- HCT Ablation Study
- SHAP Feature Importance
- Learning Curves
- Ordinal Error Analysis
- Friedman Statistical Test

---

## Project Structure

```text
Hemoglobin-Independent-Anemia-Severity/
│
├── notebooks/
│   └── anemia_severity_prediction.ipynb
│
├── results/
│   ├── metrics/
│   │   ├── model_performance.csv
│   │   ├── classification_report.csv
│   │   ├── confusion_matrix.csv
│   │   └── ablation_study.csv
│   │
│   └── plots/
│       ├── randomforest_confusion_matrix.png
│       ├── xgboost_confusion_matrix.png
│       ├── lightgbm_confusion_matrix.png
│       ├── lightgbm_confusion_matrix_no_HCT.png
│       ├── shap_global_importance.png
│       ├── shap_severe_class.png
│       └── learning_curves.png
│
├── requirements.txt
└── README.md
```

## Notebook

The complete experiment is provided in:

notebooks/anemia_severity_prediction.ipynb

The notebook contains the full workflow:

1. Data loading and preprocessing
2. Clinically grounded severity labeling
3. Feature selection without Hb
4. Model training and 5-fold cross-validation
5. Performance evaluation
6. HCT ablation study
7. SHAP explainability
8. Learning curve analysis
9. Ordinal and statistical analysis

---

## Results

Numerical results are stored in:

results/metrics/

Visual results and research figures are stored in:

results/plots/

---

## Requirements

Install the required dependencies:

pip install -r requirements.txt

Main libraries:

Pandas · NumPy · Scikit-learn · XGBoost · LightGBM · SHAP · Matplotlib · SciPy

---

## Dataset

The project uses a hematological dataset containing demographic and blood-related features.

The dataset is **not included** in this repository.

---

## Research Paper

**Title:** *Explainable Machine Learning for Hemoglobin-Independent Anemia Severity Prediction using LightGBM*

**Publication:** IEEE  
**Status:** Forthcoming

---

## Disclaimer

This project is intended for academic and research purposes only. The models should not be used as a substitute for professional medical diagnosis or clinical decision-making.

---

## Author

**Piyal Saha**
