# 📈 Stock Market Predictor using Ridge Regression

> ML-based stock price prediction model using Ridge Regression — built as Project Lead for academic project exhibition at VIT Bhopal University.
> **Grade: S (Outstanding — Highest Possible)**

---

## 📌 Overview

Stock market prediction is one of the most challenging problems in financial forecasting due to multicollinearity, overfitting, and high noise levels in financial data. This project tackles these issues using **Ridge Regression** — a regularized linear regression technique that adds a penalty term to reduce model complexity and prevent overfitting.

The model was trained on approximately **1000 daily stock price records** and achieves a prediction error of around **5% of the average stock price** (RMSE), consistently outperforming baseline linear regression.

---

## 🧠 How It Works

1. **Data Collection** — ~1000 daily records sourced from a financial API (open, close, high, low, volume)
2. **Preprocessing** — Missing value handling, feature normalization, lag variable creation
3. **Model Training** — Ridge Regression trained using scikit-learn with alpha tuning
4. **Evaluation** — RMSE metric + cross-validation for generalization testing
5. **Visualization** — Predicted vs actual price plots using Matplotlib/Seaborn

---

## 🛠️ Tech Stack

| Category | Tools |
|---|---|
| Language | Python 3.x |
| ML Library | scikit-learn |
| Data Manipulation | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Data Source | Financial API |

---

## 📊 Model Performance

| Metric | Value |
|---|---|
| Dataset Size | ~1000 daily records |
| Primary Metric | RMSE |
| Prediction Error | ~5% of average stock price |
| Validation | K-fold Cross Validation |
| vs Baseline | Outperforms standard Linear Regression |

---

## 🚀 How to Run

```bash
# Install dependencies
pip install pandas scikit-learn matplotlib seaborn numpy

# Run the predictor
python stock_predictor.py
```

```python
from sklearn.linear_model import Ridge
from sklearn.model_selection import cross_val_score
import pandas as pd

# Load and preprocess data
df = pd.read_csv('stock_data.csv')

# Train Ridge Regression model
model = Ridge(alpha=1.0)
model.fit(X_train, y_train)

# Predict
predictions = model.predict(X_test)
```

---

## ⚠️ Limitations

- Model trained and evaluated on a fixed historical dataset — not a live real-time system
- Stock predictions are inherently probabilistic and should not be used for actual trading decisions
- Does not account for external factors like news sentiment, political events, or market shocks

---

## 👥 Team

| Name | Roll No | Role |
|---|---|---|
| **Aishik Banerjee** | **22MIM10003** | **Project Lead** |
| Himangan Ghosh | 22MIM10002 | Developer |
| Chandan Kr. Singh | 22MIM10091 | Developer |
| Harsh | 22MIM10136 | Developer |
| Abhishek Nashine | 22MIM10064 | Developer |

**Guide:** Dr. Jyoti Chauhan, VIT Bhopal University
**Institution:** VIT Bhopal University — School of Computing Science, Engineering & AI
**Year:** 2025
