# Time-Series-Forecasting
# 📈 Retail Sales Forecasting Project: Guayas Region

**Course:** Data Science & Machine Learning  
**Project Focus:** Time Series Forecasting for Retail Inventory  
**Date:** January 2026

## 🚀 Project Overview
This project focuses on building a robust demand forecasting system for retail stores in the **Guayas region of Ecuador**. Using a dataset of historical sales, promotions, and economic indicators (like oil prices), I developed and compared three distinct machine learning architectures to identify the most accurate model for inventory optimization.

## 📊 The Challenge
Retail forecasting in Guayas is complex due to:
* **High Volatility:** Frequent sales spikes driven by local promotions.
* **External Factors:** The impact of fluctuating oil prices on the local economy.
* **Seasonality:** Strong weekly patterns and national holiday effects.



## 🛠️ Tech Stack & Models
* **Language:** Python 3.x (Google Colab)
* **Libraries:** Pandas, NumPy, Matplotlib, Scikit-Learn, Prophet, TensorFlow
* **Models Implemented:**
  1. **XGBoost:** Gradient Boosted Decision Trees for high-precision local pattern matching.
  2. **LSTM (Long Short-Term Memory):** Recurrent Neural Network for deep sequential learning.
  3. **Facebook Prophet:** Additive model for business-level trend and holiday decomposition.

## 🏆 Final Model Performance
After rigorous testing on the March 2014 "hold-out" set, the results were as follows:

| Model | MAE (Mean Error) | RMSE (Variance) | Forecast Bias | Verdict |
| :--- | :---: | :---: | :---: | :--- |
| **XGBoost** | **3.06** | **6.71** | **0.34** | **🏆 Best Performer** |
| **LSTM** | 7.02 | 14.98 | -0.70 | Reliable Baseline |
| **Prophet** | 74.57 | 87.08 | 73.87 | Poor / Over-fit |



## 💡 Key Findings & Recommendations
* **XGBoost is the Winner:** With an average error of only **3.06 units**, it is the recommended model for daily automated ordering in Guayas stores.
* **Avoid "Stock-Outs":** The LSTM showed a negative bias (-0.70), indicating a risk of under-stocking if used alone.
* **Business Insights:** Prophet provided valuable "Component Plots" showing that **Saturdays and Sundays** represent the highest sales volume for the region, which is critical for staffing and logistics.



## 📁 Repository Structure
* `/notebooks`: Contains `data_prep.ipynb`, `model_xgboost.ipynb`, `model_lstm.ipynb`, and `model_prophet.ipynb`.
* `requirements.txt`: List of required Python libraries.

## 📝 How to Run
1. Clone this repository.
2. Install dependencies: `pip install -r requirements.txt`
3. Open the notebooks in Google Colab and ensure your Google Drive is mounted to access the `guayas_prepared.csv` file.
