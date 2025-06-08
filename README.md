🌞 Solar Energy Prediction Model

Objective:

To develop a machine learning model that accurately predicts Global Tilted Irradiance (GTI Clean), a key indicator of solar energy potential, using weather and temporal data.

🔧 Methodology

Model Type: Supervised Regression (Random Forest Regressor)

Dataset: Historical weather and irradiance measurements

Target Variable: gti_clean (W/m²)

Input Features:

Weather data: ghi_pyr_1, ghi_pyr_2, dhi_pyr, air_temperature, humidity, wind_speed, etc.
Engineered time features: hour_sin, dayofyear_cos, etc.

📈 Performance Metrics
| Metric   | Value     | Interpretation                             |
| -------- | --------- | ------------------------------------------ |
| MAE      | 8.64 W/m² | Average prediction error                   |
| RMSE     | 17.74 W/m²| Penalizes larger errors                    |
| R² Score | 0.9975    | Explains 96% of the variance in GTI values |

The model demonstrates high accuracy, with predictions closely aligned to actual GTI values.

📊 Key Insights

Time-based patterns (hour of day, season) significantly enhance predictive power.
Strongest feature correlations include ghi_pyr_1, ghi_pyr_2, and dhi_pyr.
Residual errors are well-distributed, indicating unbiased performance.

Complete pipeline in:

Python script (.py)
Jupyter Notebook (.ipynb)
