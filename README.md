Predicting Employee Attrition
Capstone project scaffold for Predicting Employee Attrition with advanced EDA, feature engineering, and modeling.

✅ Objective
Predict employee attrition and provide actionable insights for HR through:

Exploratory Data Analysis (EDA) with interpretive comments.
Feature importance and risk factor identification.
Predictive modeling with explainability.


📂 Project Structure
data/
  ├─ raw/        # Original datasets
  ├─ clean/      # Processed datasets and EDA outputs
      └─ eda/
          ├─ univariate/
          │    ├─ figures/
          │    └─ tables/
          ├─ bivariate/
          │    ├─ figures/
          │    └─ tables/
          └─ multivariate/
               ├─ figures/
               └─ tables/
notebooks/
  ├─ Bootcamp_Data_Analysis  # Main analysis notebook
  └─Bootcamp_Git_Admin  # Git-Hub Analisys
src/
  ├─ data_prep.py
  ├─ eda_utils.py
  └─ model_utils.py
models/
  └─ trained_model.pkl
reports/
  ├─ figures/
  └─ slides/


▶ How to Run

Create a virtual environment:
Shellpython -m venv .venvMostrar mais linhas

Activate and install dependencies:
Shellsource .venv/bin/activate   # Linux/Mac.venv\Scripts\activate      # Windowspip install -r requirements.txtMostrar mais linhas

Start Jupyter Notebook:
Shelljupyter notebookMostrar mais linhas

Open:
notebooks/Enterprise_Data_Science_Bootcamp_Project.ipynb

and run the cells in order.


🔍 Features of the Updated Notebook

Automated EDA:

Univariate: distributions, outlier detection, missingness analysis.
Bivariate: Attrition vs. categorical/numeric features, risk hotspots.
Multivariate: Pearson & Spearman correlations, VIF, Cramér’s V, pairplots.


Interpretive Comments:

Each output includes what it means, how to read it, and what insights to extract.


Artifact Persistence:

All tables and plots saved under data/clean/eda/... for reproducibility.


Advanced Metrics:

Mutual Information for nonlinear signals.
Decile-based attrition profiles for monotonicity checks.



✅ Requirements
See requirements.txt. Key libraries:

pandas, numpy for data wrangling
matplotlib, seaborn for visualization
scikit-learn for modeling and feature selection
scipy for statistical utilities
ipython for rich notebook display
shap for explainability (later modeling steps)


📌 Next Steps