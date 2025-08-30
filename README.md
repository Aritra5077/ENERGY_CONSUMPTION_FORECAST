# Energy Consumption Forecasting  

Accurate energy demand forecasting is critical for ensuring **grid stability, cost efficiency and preventing shortages**.  
This project focuses on forecasting **hourly energy consumption** using **historical energy generation, weather conditions and time-based features**.  

I benchmarked **multiple Machine Learning and Deep Learning models** and found that **LSTM networks** significantly outperform traditional ML models. 

## Dataset  

- **Rows:** ~178k+ hourly records  
- **Columns:** 48 features  
- **Time Period:** Multi-year hourly dataset  
- **Target Variable:** `total load actual` (energy consumption)  

**Feature Categories:**  
- **Time-based**: hour of day, day of week, month 
- **Weather**: temperature, humidity, wind speed etc.  
- **Energy Generation**: solar, wind, hydro, nuclear contributions

  The Datasets which were used for this project are now available in
  - `Dataset/energy_dataset.csv`
  - `Dataset/weather_features.csv`

## Methodology  

1. **Data Preprocessing**  
   - *Handling missing values:* Mostly values were interpolated for a smaller amount of missing data
   - *Feature scaling & One Hot Encoding*
   - *Feature Engineering*
   - *Train-test split (time series aware)*  

2. **Exploratory Data Analysis (EDA)**  
   - Trend, seasonality, and daily patterns in consumption  
   - Correlation between weather & energy demand  
   - Visualization of various trends and oatterns in data 

3. **Modeling Approaches**  
   - **KNN**  
   - **Random Forest**  
   - **Gradient Boosting**  
   - **XGBoost**  
   - **LSTM (Deep Learning)**

4. **Evaluation Metrics**
   
   To assess forecasting accuracy, we used the following metrics:
   - **RMSE (Root Mean Squared Error):** Penalizes larger errors more strongly, useful for energy forecasting.
   - **R² (Coefficient of Determination):** Indicates how well the model explains variance in consumption.  

## Results
| Model              | RMSE     | R²      |
|--------------------|----------|---------|
| LSTM               | 964.2    | 0.9546  |
| XGBoost            | 1364.2   | 0.9091  |
| Gradient Boosting  | 1374.9   | 0.9077  |
| Random Forest      | 1502.5   | 0.8898  |
| KNN                | 1970.6   | 0.8104  |

**LSTM performed best**, effectively capturing long-term dependencies in time series data.

## Visualization  

- Energy consumption trends over time  
- Seasonal and daily load patterns  
- Predicted vs actual consumption (model comparisons)
- Residual Distribution

## Key Insights  

- Energy consumption strongly depends on **time-of-day** and **energy generation**  
- Traditional ML models capture short-term variations but fail with long dependencies  
- LSTM provides **significant performance improvement**  

## Dataset Source  

The dataset was collected from Kaggle and is available here: [Energy Consumption Dataset on Kaggle](https://www.kaggle.com/datasets/nicholasjhana/energy-consumption-generation-prices-and-weather/)
