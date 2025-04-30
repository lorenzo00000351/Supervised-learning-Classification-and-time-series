# SUP ML Pipeline: Preprocessing, Modeling, and Prediction

This repository contains a complete supervised machine learning pipeline structured across three Jupyter Notebooks:
- **Data Preprocessing**
- **Model Training & Evaluation**
- **Prediction on New Data**

---

##  Repository Structure

```bash
├── ML 1 - Preprocessing.ipynb     # Data cleaning, encoding, and feature selection
├── ML 2 - Model.ipynb             # Model training, tuning, and interpretability
├── ML 3 - Predict.ipynb           # Prediction using final model on unseen data
```

---

##  ML 1 - Preprocessing

### Key Steps:
- Exploratory Data Analysis (EDA)
  - Target distribution
  - Univariable and bivariate analysis
- Data Cleaning
  - Handling categorical variables like `crclscod`, `Area`, `ethnic`, `marital`, etc.
- Missing value imputation
- Encoding categorical features
- Feature reduction:
  - Dropping highly correlated and low variance features
- Output: Cleaned dataset saved for modeling

---

## ML 2 - Model

### Key Steps:
- Load cleaned data and split into features (`X`) and target (`y`)
- Address class imbalance via **undersampling**
- Data splitting into **train/test**
- **Rescaling** features
- **Model Tournament** with hyperparameter tuning
  - Final model selected: `CatBoostClassifier`
- Model evaluation on test set
- Interpretability: Feature importance analysis

---

## ML 3 - Predict

### Key Steps:
- Load trained model and prediction dataset
- Preprocess data to match training pipeline (encoding, scaling)
- Generate predictions
- Save prediction results for downstream use

---

## Getting Started

To run this project:
1. Clone this repository.
2. Ensure you have Python and Jupyter installed.
3. Run each notebook in order: `Preprocessing` → `Model` → `Predict`.

---

##  Requirements

Core libraries used:
- `pandas`
- `numpy`
- `scikit-learn`
- `catboost`
- `matplotlib` / `seaborn` (for EDA)

Install via:
```bash
pip install pandas numpy scikit-learn catboost matplotlib seaborn
```

---

