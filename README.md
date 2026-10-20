# Project 12: Ensemble Learning, Bagging vs. Boosting (UML501 ML Lab)

Compares a Decision Tree against Random Forest (bagging), AdaBoost and Gradient Boosting (boosting) on Breast Cancer Wisconsin (Diagnostic).

## Run
```
pip install -r requirements.txt
jupyter nbconvert --to notebook --execute --inplace ensemble_bagging_vs_boosting.ipynb
```
Or open the notebook and run all cells. About 2 minutes on a 2-core CPU, no GPU, no download (the dataset ships with scikit-learn).

## Contents
- `ensemble_bagging_vs_boosting.ipynb`: full pipeline (problem, dataset, EDA, preprocessing, baseline + methods, 3 experiments, interpretability, failure cases, conclusion, references)
- `figures/`: all plots as PNG
- `results/`: CSV tables (CV fold scores, test results, sweeps, paired tests, final summary) and `environment.txt` (versions, hardware)

## Setup notes
- Seed 42 everywhere; stratified 80/20 split; test set used once.
- Model comparison via 5x3 repeated stratified CV on the training set; sweeps use 5-fold CV; identical folds for all models.
- No scaling or imputation needed (numeric, no missing values, tree models), so no preprocessing is fitted.
- Positive class = malignant.
- Timings depend on hardware and vary slightly between runs; all other numbers are deterministic.

## Before submitting
Fill in group member names and roll numbers in the first notebook cell, and add your own words to the analysis cells so you can explain every result.
