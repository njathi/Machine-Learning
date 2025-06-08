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

Data Bias:

Bias in your data can significantly affect the accuracy, fairness, and generalizability of your solar prediction model. Here's how it might show up in your context:

🔁 1. Temporal Bias
If your dataset is heavily skewed toward:Certain months or seasons (e.g., mostly summer data), Specific times of day (e.g., mostly midday readings)
The model may perform well during those timeframes but poorly in others (e.g., winter mornings). It learns only partial seasonality.

🌍 2. Geographic or Location Bias
If your data comes from:One specific region or site, A particular terrain (e.g., only urban or coastal)
The model may not generalize well to other regions, especially those with different weather patterns or solar angles.

☁️ 3. Weather Distribution Bias
If some conditions are underrepresented, like:Cloudy days,High humidity or wind scenarios
The model may overestimate solar potential in those rare conditions because it hasn't seen enough examples of them.



This solar energy prediction model directly advances the goals of UN Sustainable Development Goal (SDG) 7: Affordable and Clean Energy by leveraging machine learning to improve the accuracy of solar irradiance forecasting. By using real-time weather and temporal data to predict solar potential, the model enables more efficient solar panel placement, energy harvesting, and grid integration—making clean energy systems more reliable and scalable. Indirectly, the model also contributes to SDG 13: Climate Action by supporting the global transition away from fossil fuels, and SDG 9: Industry, Innovation, and Infrastructure through the deployment of innovative AI solutions in energy planning. This aligns with global efforts to build sustainable and resilient energy systems through technology and data-driven strategies.
