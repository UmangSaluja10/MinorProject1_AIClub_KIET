# Breast Cancer Detection Using Supervised Machine Learning
### Minor Project 1 — AI Club, KIET Group of Institutions

---

## Problem Statement
Predict whether a breast tumor is **malignant (0)** or **benign (1)** based on 30 numerical features extracted from digitized cell-nucleus images of FNA biopsy samples.

## Dataset
| Attribute | Detail |
|---|---|
| Name | UCI Breast Cancer Wisconsin (Diagnostic) |
| Source | https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic |
| Samples | 569 |
| Features | 30 numeric |
| Target | 0 = Malignant, 1 = Benign |

## Repository Structure
MinorProject1_AIClub_KIET/
├── data/                         # Dataset (CSV)
├── model/                        # Trained models (.pkl)
├── notebook/                     # Jupyter Notebook (.ipynb)
├── results/                      # EDA plots and evaluation graphs
└── README.md

## Methodology
1. **Preprocessing** — No missing values or duplicates. Applied StandardScaler (fit on train only).
2. **EDA** — Correlation analysis, feature distributions, class balance check.
3. **Models** — Random Forest and Logistic Regression (80:20 stratified split).
4. **Evaluation** — Accuracy, Precision, Recall, F1-Score, Confusion Matrix, ROC-AUC.

## Results
| Model | Accuracy | Precision | Recall | F1-Score |
|---|---|---|---|---|
| Random Forest | 95.61% | 95.89% | 97.22% | 96.55% |
| **Logistic Regression** | **98.25%** | **98.61%** | **98.61%** | **98.61%** |

## Conclusion
Logistic Regression outperformed Random Forest (98.25% vs 95.61%), which is consistent with the near-linear separability observed in EDA. Both models exceeded the 95% recall target on the malignant class, making them viable as diagnostic decision-support tools.

## Tech Stack
Python · scikit-learn · pandas · NumPy · Matplotlib · Seaborn