# Energy Consumption Forecasting

This project focuses on forecasting **hourly energy consumption** using historical energy generation, weather conditions and time-based features.  
Accurate forecasting is crucial for **power grid management, cost efficiency, and preventing energy shortages**.  

We experimented with multiple **Machine Learning** and **Deep Learning** models to identify the most effective approach.

## Project Workflow
1. **Data Preprocessing**  
   - Handling missing values  
   - Feature engineering (time-based, weather-based, lag features)  
   - Train-test split for time series  

2. **Exploratory Data Analysis (EDA)**  
   - Trend & seasonality of energy consumption  
   - Correlation with weather & time features
   - Visualization of different trends and patterns in data

3. **Modeling**  
   - Classical ML Models: XGBoost, Gradient Boosting, Random Forest, KNN
   - Deep Learning: Long Short-Term Memory (LSTM)

4. **Evaluation Metrics**  
   - RMSE (Root Mean Squared Error)  
   - R² (Coefficient of Determination)

## Results
| Model              | RMSE     | R²      |
|--------------------|----------|---------|
| LSTM               | 964.2    | 0.9546  |
| XGBoost            | 1364.2   | 0.9091  |
| Gradient Boosting  | 1374.9   | 0.9062  |
| Random Forest      | 1485.3   | 0.8947  |
| Linear Regression  | 2436.7   | 0.7512  |

**LSTM performed best**, capturing long-term dependencies in time series data.

## Key Takeaways
- Energy consumption shows strong **daily & seasonal patterns**.  
- Weather features (temperature, humidity, etc.) improved forecasting accuracy.  
- Deep Learning (LSTM) outperformed traditional ML models.  
