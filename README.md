# 🧠 An Interpretable Machine Learning Framework for Estimating Postmortem Interval (PMI)

This project introduces an **interpretable machine learning framework** for estimating the *postmortem interval (PMI)* using multivariate forensic indicators.  
It combines scientific realism (via synthetic data generation) with transparent predictive modeling to support forensic investigations and enhance evidentiary reliability.

---

## 🔍 Overview
- Synthetic dataset generated using **Newton’s law of cooling**, **decomposition**, and **insect-activity** heuristics.  
- Models evaluated: **Lasso Regression**, **Random Forest**, **XGBoost**, **Explainable Boosting Machine (EBM)**, and **Generalized Additive Model (GAM)**.  
- Interpretability achieved through **SHAP**, **EBM component plots**, and **Partial Dependence Plots (PDPs)**.  
- Built and tested entirely in **Google Colab**, ensuring full reproducibility.

---

## 🚀 Getting Started
You can open any notebook directly in Colab using the links below or clone the repository locally.

```bash
git clone https://github.com/RefinedReinassance/pmi-interpretable-ml.git
cd pmi-interpretable-ml
pip install -r requirements.txt
```

Run the notebooks in order (01 → 04) to reproduce all experiments and visualizations.
pmi-interpretable-ml/
├─ data/                     # Synthetic & processed datasets
├─ notebooks/                # 01–04 Colab notebooks
├─ models/                   # Saved trained models
├─ interpretability_figures/  # SHAP & EBM visualizations
├─ report/                   # Final capstone report
├─ requirements.txt
├─ .gitignore
└─ README.md

📘 Notebooks
| Notebook                    | Description                                           | Open in Colab                                                                                                                                                                                                        |
| --------------------------- | ----------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 01_data_generation          | Synthetic data creation                               | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RefinedReinassance/pmi-interpretable-ml/blob/main/notebooks/01_data_generation.ipynb)          |
| 02_exploratory_analysis     | Exploratory Data Analysis (EDA) & feature engineering | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RefinedReinassance/pmi-interpretable-ml/blob/main/notebooks/02_exploratory_analysis.ipynb)     |
| 03_model_training_and_shap  | Model training + SHAP interpretability                | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RefinedReinassance/pmi-interpretable-ml/blob/main/notebooks/03_model_training_and_shap.ipynb)  |
| 04_ebm_and_interpretability | Interpretable ML (EBM & GAM visualizations)           | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RefinedReinassance/pmi-interpretable-ml/blob/main/notebooks/04_ebm_and_interpretability.ipynb) |

⚙️ Requirements

All dependencies are listed in requirements.txt.

To install manually:
pip install -r requirements.txt

Google Colab users do not need to install dependencies manually; all libraries are preloaded.

📊 Results Summary
| Model             |  MAE (h) | RMSE (h) |        R² | Notes                    |
| :---------------- | -------: | -------: | --------: | :----------------------- |
| Lasso Regression  |     4.90 |     6.67 |     0.921 | Linear baseline          |
| **Random Forest** | **3.24** | **4.63** | **0.962** | Best performance         |
| XGBoost           |     3.29 |     4.55 |     0.963 | Similar to RF            |
| EBM               |      4.2 |      5.3 |      0.93 | Highest interpretability |

Key Predictors:
body_temp_c, ambient_temp_c, decomposition_score, insect_activity_index, and humidity_pct.

Interpretability:
SHAP and EBM plots consistently revealed biologically valid trends — lower body temperature and higher decomposition scores corresponded to longer PMIs.
📈 Visual Insights

Correlation Heatmap: Visualizes feature interrelations across all forensic indicators.

Predicted vs True PMI Scatterplot: Shows model accuracy alignment.

SHAP Summary Plot: Highlights dominant predictors and their influence direction.

EBM Feature Plot: Confirms monotonic relationship between temperature decay and PMI.

(Visuals available in /interpretability_figures and generated automatically via Notebooks 03–04.)
📘 Academic Context

This work forms part of the Sol Plaatje University Capstone Project (NMST731).
It aims to bridge the gap between forensic pathology and interpretable artificial intelligence by producing a scientifically grounded, transparent predictive framework.

📧 Contact

Student: Happy Kgatle
Student Number: 202230990
Supervisor: Dr Silas Verkijika
Institution: Sol Plaatje University

🧾 Citation

If referencing this project:

Kgatle, H. (2025). An Interpretable Machine Learning Framework for Estimating Postmortem Interval Using Multivariate Forensic Indicators. Sol Plaatje University.

🏆 Acknowledgements

Special thanks to Dr Silas Verkijika,Ibidun for supervision and guidance, and to the Sol Plaatje University Department of Computer Science for providing computational resources and support.
