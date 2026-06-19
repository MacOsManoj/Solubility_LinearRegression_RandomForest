# Solubility Prediction — Linear Regression & Random Forest

A Google Colab notebook that predicts aqueous solubility (logS) of chemical compounds using molecular descriptors, comparing **Linear Regression** and **Random Forest** regression models.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MacOsManoj/Solubility_LinearRegression_RandomForest/blob/main/Solubility.ipynb)

## Overview

This project uses the **Delaney solubility dataset** (1,144 compounds) to build regression models that predict molecular solubility from computed chemical descriptors. It serves as a practical introduction to cheminformatics-style ML.

## Dataset

| Feature | Description | Range |
|---|---|---|
| `MolLogP` | Partition coefficient (lipophilicity) | −7.57 to 10.39 |
| `MolWt` | Molecular weight (g/mol) | 16.04 to 780.95 |
| `NumRotatableBonds` | Count of rotatable bonds | 0 to 23 |
| `AromaticProportion` | Fraction of aromatic atoms | 0.0 to 1.0 |
| **`logS`** (target) | Log aqueous solubility | −11.6 to 1.58 |

Source: [Delaney solubility dataset](https://raw.githubusercontent.com/dataprofessor/data/refs/heads/master/delaney_solubility_with_descriptors.csv)

## Workflow

1. **Load Data** — Fetch the CSV dataset directly from GitHub
2. **Data Preparation** — Separate features (`X`) and target (`y = logS`)
3. **Train/Test Split** — 80/20 split (`random_state=100`)
4. **Model Building** — Train Linear Regression and Random Forest regressors
5. **Evaluation** — Compare model performance metrics (MSE, R²)

## Tech Stack

- **Python 3** (Google Colab)
- **pandas** — data loading & manipulation
- **scikit-learn** — `train_test_split`, `LinearRegression`, `RandomForestRegressor`
