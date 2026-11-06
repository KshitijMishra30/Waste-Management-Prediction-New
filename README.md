# Waste Management India – Daily Waste Generation Prediction

## Overview
A supervised **regression** project to estimate `Daily_Waste_Generation_Tons`, a continuous target representing daily waste generation in tons.

## Project workflow
- Loaded and inspected the India waste-management dataset.
- Checked missing values, duplicates and descriptive statistics.
- Applied domain-driven feature selection, excluding `City`, `Region` and `Season` from model inputs as documented in the notebook.
- Performed exploratory analysis of waste generation by waste type, city category, state and year.
- Examined target skewness and used a log transformation for model training.
- Encoded categorical variables, split the data into training and testing sets, and scaled inputs for selected models.
- Compared Linear Regression, Decision Tree, Random Forest and K-Nearest Neighbors regression models.
- Evaluated models using R², MAE and RMSE, then performed hyperparameter tuning.
- Included functions for city/state-level daily waste estimates.

## Tools
Python, Jupyter Notebook, Pandas, NumPy, Matplotlib, Seaborn, SciPy, Scikit-learn.

## Repository structure
```text
.
├── waste_management_prediction.ipynb
├── data/
│   └── README.md
├── requirements.txt
├── .gitignore
└── README.md
```

## Dataset
The notebook expects `data/Waste_Management_India.csv`. The dataset is not included. Place the CSV in `data/` and verify its source license before sharing it publicly.

## Run locally
```bash
pip install -r requirements.txt
jupyter notebook
```
Open `waste_management_prediction.ipynb` and run cells in order.

## Notes
The notebook documents manual encoding/scaling and does not use an sklearn Pipeline or SimpleImputer. Its city-level prediction function estimates combined waste across the waste types represented by the model; see the notebook's notes for assumptions.

## Author
Kshitij Mishra
