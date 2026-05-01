# House Price Prediction using Machine Learning

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python" />
  <img src="https://img.shields.io/badge/scikit--learn-ML-orange?style=for-the-badge&logo=scikit-learn" />
  <img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter" />
  <img src="https://img.shields.io/badge/Status-Complete-brightgreen?style=for-the-badge" />
</p>

> A machine learning project that predicts residential house prices based on structural features such as living area, bedrooms, bathrooms, floors, and view quality — trained on a real-world dataset of 4,600 records.

---

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Methodology](#methodology)
- [Results](#results)
- [Getting Started](#getting-started)
- [Future Scope](#future-scope)
- [Author](#author)

---

## Overview

House price prediction is a fundamental problem in real estate analytics. This project builds a **Linear Regression** model that learns from historical property data to estimate house prices for new inputs.

The end-to-end pipeline covers data loading, cleaning, exploratory analysis, feature selection, model training, prediction, and evaluation — following standard machine learning best practices.

---

## Dataset

| Property | Details |
|---|---|
| **Source** | [Kaggle](https://www.kaggle.com/) |
| **Total Records** | 4,600 |
| **File** | `data.csv` |
| **Target Variable** | `price` (USD) |

### Features Used

| Feature | Description |
|---|---|
| `sqft_living` | Living area in square feet |
| `bedrooms` | Number of bedrooms |
| `bathrooms` | Number of bathrooms |
| `floors` | Number of floors |
| `view` | View quality rating (0–4) |

---

## Tech Stack

| Tool | Purpose |
|---|---|
| **Python 3.x** | Core language |
| **pandas** | Data manipulation |
| **NumPy** | Numerical operations |
| **matplotlib** | Plotting & visualization |
| **seaborn** | Statistical visualizations |
| **scikit-learn** | ML model & evaluation |
| **Jupyter Notebook** | Interactive development |

---

## Project Structure

```
house-price-prediction/
 data.csv              # Raw dataset (4,600 records)
 data.dat              # Processed data file
 main_final.ipynb      # Final model notebook (training + evaluation)
 main_trail.ipynb      # Experimental / trial notebook
 output.csv            # Model prediction results
 report.ipynb          # Full project report
 README.md             # Project documentation
```

---

## Methodology

```
Data Loading → Data Cleaning → EDA & Visualization
     ↓
Feature Selection → Train/Test Split (80/20)
     ↓
Linear Regression Training → Prediction → Evaluation
```

1. **Data Loading** — Load `data.csv` with pandas; inspect shape, types, and stats
2. **Data Cleaning** — Handle nulls, duplicates, and data type inconsistencies
3. **EDA** — Histograms, scatter plots, and correlation heatmap
4. **Feature Selection** — 5 features selected based on correlation with `price`
5. **Model Training** — `LinearRegression` from scikit-learn on 80% of data
6. **Prediction** — Generate predictions on 20% test split
7. **Evaluation** — Measured using MSE and RMSE

---

## Results

| Metric | Value |
|---|---|
| **Mean Squared Error (MSE)** | 989,906,638,552.23 |
| **Root Mean Squared Error (RMSE)** | ~$994,940 |

> The model captures the general trend of house prices. The high RMSE reflects the wide price variance in the dataset — this is a solid baseline that can be improved with feature engineering and advanced models.

---

## Getting Started

### Prerequisites

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Clone the Repository

```bash
git clone https://github.com/Bitttu4/house-price-prediction.git
cd house-price-prediction
```

### Run the Notebook

```bash
jupyter notebook main_final.ipynb
```

---

## Future Scope

- [ ] Include additional features: `zipcode`, `lat/long`, `yr_built`, `sqft_lot`
- [ ] Try advanced models: **Random Forest**, **XGBoost**, **Gradient Boosting**
- [ ] Apply **k-fold cross-validation** for robust evaluation
- [ ] Use **hyperparameter tuning** (GridSearchCV)
- [ ] Build a **Streamlit / Flask web app** for real-time predictions
- [ ] Explore **deep learning** approaches with TensorFlow/Keras

---

## Author

**Bitttu4**  
 [GitHub Profile](https://github.com/Bitttu4)  
 [Repository](https://github.com/Bitttu4/house-price-prediction)

---

<p align="center"> If you found this project useful, please give it a star!</p>
