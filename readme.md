# Diabetes Dataset Analysis and Modeling

Brief: EDA, preprocessing, classification and clustering on a clinical diabetes dataset using a Jupyter notebook.

## Repository structure
- notebook.ipynb — main notebook with all analysis and modeling steps.
- Dataset of Diabetes .csv — input data (place in repo root).
- readme.md — this file.

## Dataset
- 1000 samples, ~16 columns (AGE, Urea, Cr, HbA1c, Chol, TG, HDL, LDL, VLDL, BMI, Gender, CLASS, etc.).
- Target: CLASS (N, P, Y) — note class imbalance and some label/typo issues cleaned in notebook.

## Requirements
* Python 3.8+ and:
* pip install pandas numpy matplotlib seaborn scikit-learn 
xgboost statsmodels scipy jupyter

## Quick start
1. Ensure `Dataset of Diabetes .csv` is in the project folder.
2. Open the notebook:
   - Jupyter: jupyter notebook notebook.ipynb
   - VS Code: open notebook.ipynb and run cells.
3. Run cells sequentially to reproduce results.

## Notable steps in notebook
- Cleaning: Gender and CLASS typos fixed; ID and No_Pation dropped.
- EDA: distributions, boxplots, clinical-range summaries.
- Multivariate: correlation heatmaps, VIF for multicollinearity.
- Modeling: Logistic Regression, Random Forest, XGBoost with GridSearchCV and evaluation (confusion matrices, ROC/AUC).
- Clustering: KMeans, Agglomerative, DBSCAN with PCA/t-SNE visualizations.

## Findings & notes
- Lipid features show multicollinearity (check VIF).
- Creatinine values appear scaled; verify units.
- Classes are imbalanced — consider resampling (SMOTE) for further work.
- Models and visualizations are implemented in the notebook; metrics printed/visualized there.

## Contact
For issues or improvements, open an issue or edit the notebook directly.