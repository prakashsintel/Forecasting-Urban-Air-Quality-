**Forecasting Urban Air Quality Using Time-Series Models**

**Team Members**
Shivam Kumar — kshivam@iisc.ac.in

Sachin R — sachinr@iisc.ac.in

Prakash S — prakashs1@iisc.ac.in

Pothukanuri Sai Venkat — saivenkatp@iisc.ac.in

**Problem Statement**
Air pollution poses a major health and environmental challenge in India. Cities such as Delhi frequently suffer from hazardous air quality episodes driven by traffic, industrial emissions, meteorology, biomass burning, and seasonal variations.
Despite the urgency, citizens and authorities lack an early-warning system capable of forecasting AQI levels in advance. A reliable short-term AQI forecasting tool can support:
- Public health advisories
- Policy decisions and traffic regulation
- Pollution control operations
- Personal planning for sensitive groups
This project aims to address this gap through data-driven forecasting.

**Dataset Description**
The dataset is sourced from the Central Pollution Control Board (CPCB) and made publicly available through:
- Open Government Data (OGD) Platform India
- Kaggle (compiled datasets)
The data is provided in CSV format and contains multi-year (e.g., 2015–2022) hourly and daily measurements from several monitoring stations of Indian metropolitan cities.

**Included Features**
- Pollutants: PM2.5, PM10, NO₂, SO₂, CO, O₃
- Meteorological parameters: Temperature, humidity, wind speed, etc.
- Timestamp: Hourly or daily resolution
- Target: Derived Air Quality Index (AQI) based on CPCB standards
The dataset provides a rich basis for time-series forecasting, capturing both long-term trends and seasonal behavior.

**Objective**
To build a robust forecasting model capable of predicting the next 24–72 hours of AQI values for a major Indian city (e.g., Delhi).
The system should:
- Capture seasonal variations and autocorrelation
- Respond to short-term fluctuations
- Handle noisy and missing data
- Provide accurate, interpretable predictions

**High-Level Approach**
1. Data Preprocessing
- Resampling hourly data to daily averages
- Handling missing values (interpolation / forward fill)
- Smoothing and noise reduction
- Feature engineering (lags, rolling averages, seasonal indicators)
2. Baseline Models
- Simple Moving Average (SMA): A naïve baseline that smooths the series using the average of previous N days.
- Exponential Moving Average (EMA): A faster-responding baseline giving higher weight to recent observations.
These serve as reference points to measure the improvement of advanced models.
3. Advanced Forecasting Models
- SARIMA : Captures seasonal patterns, models trend + seasonality + autocorrelation. Strong for classical time-series with periodic behavior.
- LSTM (Long Short-Term Memory) : Deep-learning model for sequence data. Learns long-term dependencies and non-linear patterns, handling complex relationships between pollutants and meteorology.
- XGBoost (Extreme Gradient Boosting) : State-of-the-art tree-based model. Excellent for tabular time-series with engineered lag features, handling missing data and non-linear interactions effectively. Often outperforms neural networks in real-world AQI forecasting.
4. Evaluation Metrics
The models are evaluated using standard regression and categorical metrics:
- MAE (Mean Absolute Error)
- RMSE (Root Mean Square Error)
- MAPE (Mean Absolute Percentage Error)
- R² Score
- AQI Category Accuracy (Correct classification into Good / Moderate / Unhealthy etc.)

**Summary**

This project builds a complete AQI forecasting pipeline integrating:
- Classical statistical models (SMA, EMA, SARIMA)
- Deep learning (LSTM)
- Machine learning (XGBoost / Gradient Boosting)
The goal is to provide accurate short-term AQI predictions that can support public health decision-making and environmental management.
Our final system outputs:
- Next 24–72 hour AQI forecasts
- Visualization plots for actual vs predicted values
- Performance metrics for all models
- Best performing model recommendation
The long-term objective is to extend this into a real-time AQI forecasting dashboard that can be deployed for any major Indian city.
