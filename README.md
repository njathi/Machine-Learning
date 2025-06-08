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
| Metric   | Value     | Interpretation                                |
| -------- | --------- | --------------------------------------------- |
| MAE      | 8.64 W/m² | Average prediction error                      |
| RMSE     | 17.74 W/m²| Penalizes larger errors                       |
| R² Score | 0.9975    | Explains 99.75% of the variance in GTI values |

The model demonstrates high accuracy, with predictions closely aligned to actual GTI values.

📊 Key Insights

Time-based patterns (hour of day, season) significantly enhance predictive power.
Strongest feature correlations include ghi_pyr_1, ghi_pyr_2, and dhi_pyr.
Residual errors are well-distributed, indicating unbiased performance.

Complete pipeline in:

Python script (.py)

Jupyter Notebook (.ipynb)


✅ 1. MAE – Mean Absolute Error
MAE: 8.64
What it means: On average, the model's predictions are off by about 8.64 W/m².

If gti_clean values typically range between 0–1000 W/m², an error of 8.64 is quite small (~1%).

The model is reasonably accurate in predicting solar irradiance.

✅ 2. RMSE – Root Mean Squared Error
RMSE: 17.74
What it means: Similar to MAE, but penalizes larger errors more heavily.

It helps detect outliers or occasional large mistakes.

RMSE > MAE suggests there are some larger deviations, but overall performance is still solid.

✅ 3. R² Score – Coefficient of Determination
python
Copy
Edit
R² Score: 0.9975
What it means: 99.75% of the variability in solar irradiance is explained by the model’s input features.

A perfect model would have R² = 1.0.

The model is capturing the major patterns in the data very well.

📊 Visual Aids in the Notebook:

Actual vs Predicted Plot

Points close to the diagonal line mean accurate predictions.

A tight, linear pattern confirms high R².

Residual Distribution Plot

If residuals are centered around zero and roughly normal, it means the model's errors are unbiased and well-distributed.

Correlation Heatmap & Feature Plots

Helps validate that important weather features (like GHI, temperature, etc.) have strong relationships with GTI.

🎯 Overall Evaluation:
Your Random Forest model shows:

High accuracy

Low prediction error

Robust performance even with variability in weather
