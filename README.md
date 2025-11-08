# An Interpretable Machine Learning Framework for Estimating Postmortem Interval (PMI)

This repository contains the code, notebooks, and data for a capstone project that develops an **interpretable machine learning framework** to estimate Postmortem Interval (PMI) from synthetic forensic indicators.

---

## 🔍 Overview
- Synthetic dataset generated using Newton’s law of cooling, decomposition, and insect-activity heuristics.
- Models: Linear (Lasso), Random Forest, XGBoost, Explainable Boosting Machine (EBM), and Generalized Additive Model (GAM).
- Interpretability: SHAP explanations, EBM component plots, and Partial Dependence Plots (PDPs).
- Built and tested in **Google Colab**.

---

## 📂 Repository structure
pmi-interpretable-ml/
├─ data/ # Synthetic & processed datasets
├─ notebooks/ # 01–04 notebooks
├─ models/ # Saved trained models
├─ interpretability_figures/ # SHAP & EBM visualizations
├─ report/ # Final report document
├─ requirements.txt
├─ .gitignore
└─ README.md


---

## ▶️ Run notebooks in Google Colab
| Notebook | Description | Open |
|-----------|--------------|------|
| 01_data_generation | Create the synthetic dataset | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/<RefinedReinassance>/pmi-interpretable-ml/blob/main/notebooks/01_data_generation.ipynb) |
| 02_exploratory_analysis | EDA + feature engineering | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/<RefinedReinassance>/pmi-interpretable-ml/blob/main/notebooks/02_exploratory_analysis.ipynb) |
| 03_model_training_and_shap | Model training + SHAP | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/<RefinedReinassance>/pmi-interpretable-ml/blob/main/notebooks/03_model_training_and_shap.ipynb) |
| 04_ebm_and_interpretability | Interpretable models (EBM/GAM) | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/<RefinedReinassance>/pmi-interpretable-ml/blob/main/notebooks/04_ebm_and_interpretability.ipynb) |

---

## ⚙️ Requirements
Install dependencies (Colab installs automatically):
pip install -r requirements.txt


---

## 📊 Results summary
- **Best model:** Random Forest / EBM (MAE ≈ 3 – 5 h)  
- **Key predictors:** body_temp_c, ambient_temp_c, decomposition_score, insect_activity_index  
- **Interpretability:** EBM and SHAP consistently show physically meaningful relationships.

---

## 📧 Contact
**Student:** Happy Kgatle
**Student N.O** 202230990
**Supervisor:** Dr Silas Verkijika  
**Institution:** Sol Plaatje University



