# RTSM: Real-Time Temperature Forecasting
### Comparative Analysis of Regularized Regression and Seasonal Stochastic Models

This project investigates various statistical and machine learning approaches to predict daily minimum temperatures. By comparing traditional **Stochastic Time-Series models (ARIMA/SARIMA)** with **Regularized Regression (Lasso, OLS)** and **Non-linear Polynomial models**, this research identifies the most stable and accurate methods for environmental forecasting.

---
## 👨‍🔬 Authors
@aarushisharma1623
@anuj-10k
@DrustO9
@jatinofficial4001
@KrishnaRai1
@24Sudhanshu

## 📊 Project Overview
The core objective is to evaluate how different mathematical frameworks handle the inherent seasonality and autocorrelation found in climate data. 

### Key Features:
* **Time-Series Decomposition:** Extracting Trend, Seasonality, and Residual components.
* **Feature Engineering:** Lag-based features ($t-1$, $t-7$), Rolling Statistics (7-day mean), and Temporal indicators (Day of Year).
* **Statistical Diagnostics:** ADF tests for stationarity, ACF/PACF plots, and Normality checks (Q-Q plots).
* **Model Benchmarking:** Comparison of 8 different modeling techniques based on RMSE and MAE.

---

## 🛠️ Tech Stack
* **Language:** Python 3.x
* **Libraries:** * `pandas` & `numpy`: Data manipulation
    * `statsmodels`: ARIMA, SARIMA, and OLS regression
    * `scikit-learn`: Linear, Lasso, and Polynomial regression
    * `seaborn` & `matplotlib`: Advanced data visualization

---

## 📈 Model Performance Summary
Based on the testing conducted in the [RTSM_PROJECT.ipynb](https://colab.research.google.com/drive/1fY4Fbjt-PFs6bZ0phGb0TvjaCE5Hmit_?usp=sharing), the **Polynomial Regression (Degree 2)** emerged as the superior model.

| Rank | Model | RMSE | MAE |
| :--- | :--- | :--- | :--- |
| **1** | **Polynomial** | **2.2787** | **1.7644** |
| 2 | OLS / Multiple Linear | 2.3231 | 1.7958 |
| 3 | Lasso | 2.3233 | 1.7970 |
| 4 | ARIMA | 2.3361 | 1.7989 |
| 5 | SARIMA | 2.7349 | 2.1343 |

> **Key Finding:** While SARIMA accounts for seasonality, the Polynomial model captured the non-linear interactions between lagged features more effectively for this specific dataset.

---

## 🚀 How to Use
1. **Dataset:** The project uses the `daily-min-temperatures.csv` dataset (1981-1990).
2. **Run the Analysis:** * Open the notebook in [Google Colab](https://colab.research.google.com/drive/1fY4Fbjt-PFs6bZ0phGb0TvjaCE5Hmit_?usp=sharing).
    * Execute the "Data Import" and "Feature Engineering" cells.
    * Run the "Model Training" suite to generate the comparative metrics.
3. **Visualization:** Review the `Stability Plot` and `Residual PACF` to verify that the models successfully captured the signal.

---

## 🔬 Statistical Significance
The OLS Hypothesis Testing confirmed that **Lag1** and **Rolling_7** averages are the most significant predictors ($p < 0.001$), while the "Day of Year" was found to be statistically insignificant when used alongside lag features.

---

## 📂 Documentation
For a deep dive into the methodology, including the mathematical breakdown of the regression vs. stochastic approaches, refer to the [RTSM_Research_Report.docx](https://docs.google.com/document/d/1N35VCJKHp81nR1rCxanRRKyt4Igr6A1G/edit).

---