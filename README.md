# Electric Energy Consumption Time Series Analysis

## Dataset Definition
The dataset shows a comprehensive record of energy consumption every 10 minutes collected over a year (2017/1/1 0:00 - 12/30/2017 23:50) in Tetouan, Morocco. Tetousan is a city located in the north of Morocco which occupies and area of around 10375 km^2 and its population is about 550.374 inhabitants. It includes the date and time of the observations collected at 10-minute intervals, weather temperature (e.g., 6.559), weather humidity (e.g., 73.8), wind speed (e.g., 0.083), general diffuse flows which is a catchall term to describe low-temperature fluids (e.g., 0.051), diffuse flows (e.g., 0.051), zone 1 power consumption (e.g., 34055.6962), zone 2 power consumption (e.g., 16128.87538), and zone 3 power consumption (e.g., 20240.96386). In total, there are 9 columns: Datetime, Temperature, Humidity, WindSpeed, GeneralDiffuseFlows, DiffuseFlows, PowerConsumption_Zone1, PowerConsumption_Zone2, PowerConsumption_Zone3, and 52416 rows, excluding the section title. There is no missing or overlapping data. providing insights into various factors influencing electricity usage. The data spans a considerable period and is structured to facilitate detailed analysis. The dataset is meant to be used for studying the impact of energy consumption. The dataset originates from the SCADA system of Amendis, responsible for distributing electricity in Tetouan.
The dataset link is included in the project. 

## Project Objectives
1.**Examine Trends and Patterns in Energy Consumption**
- Find seasonal trends and peaks in Tetouan, Morocco's energy consumption patterns over time.
- Understand consumption seasonality by examining hourly, daily and weekly fluctuations in energy demand.
2.**Examine the Impact of Weather on Energy Usage**
- Analyze how different weather conditions affect energy usage.
- Determine the relationship between weather variables (temperature, humidity) and electricity consumption.
3.**Evaluate the Performance of Various Machine Learning Models in Predicting Energy Consumption**
- Evaluate the effectiveness of different machine learning models (e.g., ARIMA, SARIMA, MLP, CNN, LSTM) in forecasting energy consumption.
- Identify the most accurate and reliable model for predicting future energy usage based on historical data.
- Compare the models based on their RMSE, MAE, and MAPE metrics to determine the best-performing model.
4.**Find the Benefits of Integrating Multiple Features for Enhanced Forecast Accuracy**
- Investigate how incorporating multiple features (temperature) can improve the accuracy of energy consumption forecasts.
- Develop and evaluate multi-input models to capture additional variability and dependencies in the data.

## Research Questions

1. **What are the trends and patterns in energy consumption over the recorded period?**
2. **How do different weather conditions affect electricity usage in Tetouan?**
3. **How effective are different machine learning models in predicting energy consumption, and which model performs the best?**
4. **How can integrating multiple features (e.g., temperature, humidity) improve the accuracy of energy consumption forecasts?**

## Project Summary
1.**What are the trends and patterns in energy consumption over the recorded period?**
- There is a seasonality which is higher energy consumption during morning and evening hours due to human activities (e.g., households, work).
- There is a trend of increasing energy usage during summer months for cooling.
- Daily seasonality is important for accurate modeling and forecasting of energy consumption.
- The prophet model was able to catch all seasonalities that the data has and differentiate them.

2.**How do different weather conditions affect electricity usage in Tetouan?**
- Temperature: There is a positive correlation (0.440) with power consumption, with higher temperatures increasing air conditioning use in summer and colder temperatures increasing heating use in winter.
- Humidity: There is a weak negative correlation (-0.287) with power consumption.
- power wind: There is almost no correlation (0.167) with power consumption.
- Temperature data was used as a feature to find demands based on the seasons or weather conditions using the classification method.

3.**How effective are different machine learning models in predicting energy consumption, and which model performs the best?**
- Naive and Drift Models: High RMSE, MAE, and MAPE values indicate limited predictive power.
- Seasonal Naive and Mean Models: Slightly better but still high error metrics.
- Autoregression and AR+MA Models: Lower RMSE and MAE, but high MAPE values.
- ARIMA and SARIMA Models: Lowest RMSE, MAE, and MAPE values, with SARIMA performing best due to capturing seasonal patterns.
- Univariate MLP and CNN Models: Low RMSE and MAE but high MAPE values suggest issues with generalization.
- Multivariate MLP and CNN Models: Slightly better RMSE and MAE but still high MAPE values.
- Multi-step Models: Higher error metrics, and it is difficult to capture multi-step dependencies accurately.
- The Prophet Model: High error for RMSE and MAE but lowest percentage for MAPE.
- The prophet model is the best-performing model across all metrics because it captures multiple seasonalities at the same time, and removes the outliers.
- The grid search succeeded in searching the best parameters for MLP, CNN and LSTM.

4.**How can integrating multiple features (e.g., temperature, humidity) improve the accuracy of energy consumption forecasts?**
 Multiple Input Models: Improved RMSE and MAE values by capturing additional variability from multiple features.
- Multi-headed and Multi-output Models: Benefit from additional features but still face high MAPE values.
- Multi-step Models: Better performance in capturing future steps but higher error metrics compared to simpler models.
- The classification succeeded in classifying the data into five labels based on the power consumption data and temperature data as a feature to investigate the usage based on weather conditions.
<br><br/>

This project thoroughly analyzed the demand and usage for power consumption based on historical data while utilizing various frameworks and methods to forecast future power consumption. The discovered patterns, trends, and accurate predictions are essential for power suppliers in determining future strategies. Therefore, it is crucial to aim for an expansion of knowledge and techniques, along with achieving even higher accuracy in predictions.

The detail insights of each analysis and results are described in the project.
