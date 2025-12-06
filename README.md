Introduction
This project delivers a fully exploratory data analysis (EDA) framework designed to support attrition studies and HR decision‑making. The workflow integrates univariate, bivariate, and multivariate analyses, producing distributions, attrition rates, correlation maps, and hotspot grids with both plots‑only and tables‑only modes for flexible artifact generation. Each output is accompanied by interpretive comments, explaining the meaning of the metric, how to read the visualization, and suggesting follow‑up actions to highlight potential risk factors. Advanced metrics such as mutual information, decile‑based attrition profiles, and Cramér’s V extend beyond traditional correlation checks to capture nonlinear signals and monotonic relationships. All artifacts are saved under a structured repository (data/clean/eda/...) with safe filenames for reproducibility. The environment relies on core libraries including pandas, numpy, matplotlib, seaborn, scikit‑learn, scipy, ipython, and shap, with optional extras like plotly and statsmodels. The notebooks (Bootcamp_Data_Analysis – Initial Exploration and Bootcamp_Data_Analysis – Simplified) and supporting modules (src/eda_utils.py, src/data_prep.py, src/model_utils.py) ensure consistent preprocessing, encoding, feature selection, and model explainability. Outputs include summary CSVs, attrition tables, correlation matrices, and a wide range of figures (histograms, bar charts, violin/boxplots, heatmaps, pairplots, hotspot grids), all organized for reproducible analysis and clear communication in reports and slides.


EDA Features
- Univariate analysis: distributions, value counts, outlier detection, missingness tables.
- Bivariate analysis: attrition distribution, attrition rate by categorical features, numeric summaries by target, risk hotspots.
- Multivariate analysis: Pearson & Spearman correlations, VIF, Cramér’s V, pairplots, 2D hotspot grids.
- Plots-only and Tables-only modes supported for flexible artifact generation.
- All outputs saved under data/clean/eda/... for reproducibility.
Interpretive Comments
- Each EDA output includes guidance on interpretation: what the metric means, how to read the visualization/table, and suggested follow-up actions for HR.
- Highlights potential risk factors and monotonic relationships where relevant.
Advanced Metrics
- Mutual Information for capturing nonlinear signals versus Pearson correlation.
- Decile-based attrition profiles for monotonicity and risk segmentation checks.
- Categorical association mapping with Cramér’s V.
Artifact Persistence
- Tables and figures saved by default to:
- data/clean/eda/univariate/tables and data/clean/eda/univariate/figures
- data/clean/eda/bivariate/tables and data/clean/eda/bivariate/figures
- data/clean/eda/multivariate/tables and data/clean/eda/multivariate/figures
- File naming uses safe filenames derived from column names.

Requirements
- See requirements.txt. Key libraries:
- pandas, numpy — data wrangling
- matplotlib, seaborn — visualization
- scikit-learn — modeling, VIF, mutual information, feature selection
- scipy — statistical utilities
- ipython — rich notebook display
- shap — explainability for model interpretation
- Optional extras: plotly, statsmodels

Notebook and Project Structure
- Notebook Bootcamp_data_Analysis - Initial Exploration highlights:
- src/eda_utils.py: safe filename generation, table/figure saving, categorical detection, plotting helpers, annotation utilities.
- src/data_prep.py: consistent encoding, train/validation splits, imputation defaults, target binarization.
- src/model_utils.py: baseline pipelines, cross-validation, feature importance export, SHAP wrappers.
- Outputs produced:
- Summary CSVs: dtype info, missingness, descriptive stats, value counts, outlier scans, missingness correlations.
- Bivariate tables: attrition rates by category, numeric summaries by target.
- Multivariate tables: Pearson/Spearman, VIF, Cramér’s V, mutual information rankings, MI feature pairs.
- Figures: histograms, countplots, attrition bar charts, violin/boxplots by target, heatmaps, pairplots, hotspot grids.

- Notebook Bootcamp_data_Analysis - Final Exploration highlights:
Selected plots and insights from Initial Exploration Notebook

- Repository layout:
- data/
- raw/
- clean/
- eda/
- univariate/{figures,tables}
- bivariate/{figures,tables}
- multivariate/{figures,tables}
- notebooks/
- Bootcamp_Data_Analysis - Initial Analysis.ipynb
- Bootcamp_Git_Admin - Simplified.ipynb
- src/
- data_prep.py
- eda_utils.py
- model_utils.py
- models/
- trained_model.pkl
- reports/
- figures/
- slides/
