# Credit Risk Prediction Using Machine Learning

This repository contains an academic machine learning project focused on **credit default prediction** using the LendingClub dataset.  
The objective is to design, evaluate, and compare several models under **realistic banking constraints**, including temporal validation, class imbalance, and economic interpretability.

The project combines:
- exploratory data analysis,
- robust preprocessing,
- multiple predictive models,
- out-of-time validation,
- and business-oriented model selection.

## Final Version of the Project

### Final Notebook

The final and authoritative implementation of the project is:

`notebooks/IF4_Derasse_Paviet_Minard_Project_CreditRisk.ipynb`

This notebook contains:
- the full data preprocessing pipeline,
- leakage detection and removal,
- temporal (OOTV) validation,
- model training and evaluation (Logistic Regression, Random Forest, XGBoost, TabNet, Decision Tree),
- economic interpretation of results,
- and final model selection.

This notebook should be considered the definitive version for grading and evaluation

### Final Report (PDF)

The final written report is available in:

`report/IF4_Derasse_Paviet_MinardCredit_Risk_Prediction___Machine_Learning.pdf`

The LaTeX source is located in:
- `report/main.tex`
- `report/figures/`

The report presents:
- the business context,
- methodological choices,
- results analysis,
- operational recommendations,
- and conclusions aligned with banking practices.

## Previous / Intermediate Versions

The repository also contains earlier or intermediate notebooks created during the development process:

- `Lab5_Project_CreditRisk.ipynb`  
- `updated version of project.ipynb`  
- `Essai_Tuning.ipynb`

These files correspond to:
- early experiments,
- hyperparameter tuning attempts,
- partial implementations.

They are kept for traceability only and should not be used for evaluation.

## Repository Structure
<img width="613" height="452" alt="image" src="https://github.com/user-attachments/assets/330f25aa-0f95-46c8-af99-51003cf0ef73" />


## Modeling Strategy (High-Level)

- Validation protocol: strict time-based split (≤2016 / 2017 / 2018 OOTV)
- Main challenge: strong class imbalance and temporal drift
- Key metrics: ROC-AUC, Recall (default), Precision (default), F1-score
- Excluded approach: SMOTE (too many false positives for banking context)

### Final model recommendations:
- Production credit scoring -> Random Forest  
- Early-warning / monitoring-> TabNet  
- Governance et explainability reference --> Optimized Decision Tree  

## Authors

- Sherynne Derasse
- Raphaël Paviet
- Basile Minard

## Dataset

The dataset used is the LendingClub Loan Dataset (2007–2018)  
Publicly available at: [https://www.lendingclub.com/](https://www.kaggle.com/datasets/wordsforthewise/lending-club)

