# Time Series Analysis and Forecasting (Kaggle Course Project)

Welcome to my project repository for the **Time Series Analysis and Forecasting** course completed on [Kaggle Learn](https://www.kaggle.com/learn/time-series). This course provided practical exposure to real-world forecasting challenges using statistical methods and machine learning models.

---

## Course Structure

The course was divided into six comprehensive lessons:

1. **Linear Regression with Time Series**  
   Applying simple and multivariate regression models on time-indexed data.

2. **Trend**  
   Identifying and modeling long-term progression using smoothing and differencing.

3. **Seasonality**  
   Understanding repetitive patterns over fixed periods using Fourier terms and decomposition.

4. **Time Series as Features**  
   Creating lag, window, and time-based features to improve model performance.

5. **Hybrid Models**  
   Combining statistical models with machine learning (e.g., residual modeling).

6. **Forecasting with Machine Learning**  
   Using gradient boosting and other ML models (e.g., XGBoost, LightGBM) for advanced forecasting tasks.

---

## Environment & Execution

All code was written and executed in **Google Colab** to take advantage of cloud computing and seamless data handling.

---

## Repository Structure

```bash
time-series-kaggle/
│
├── notebooks/          # Google Colab notebooks for each lesson
│   ├── 01_linear_regression.ipynb
│   ├── 02_trend.ipynb
│   ├── 03_seasonality.ipynb
│   ├── 04_time_series_features.ipynb
│   ├── 05_hybrid_models.ipynb
│   └── 06_ml_forecasting.ipynb
│
├── python/             # Equivalent Python scripts from notebooks
│   ├── linear_regression.py
│   ├── trend.py
│   ├── seasonality.py
│   ├── features.py
│   ├── hybrid_models.py
│   └── ml_forecasting.py
│
├── data/
│   └── sample_datasets/   # Example time series datasets
│
├── images/
│   └── plots/             # Visualizations (e.g., trends, forecasts)
│
├── README.md
└── requirements.txt
