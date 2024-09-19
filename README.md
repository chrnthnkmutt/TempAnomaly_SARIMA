Here’s a draft `README.md` for your GitHub repository `chrnthnkmutt/TempAnomaly_SARIMA` based on the provided content:

---

# TempAnomaly_SARIMA

This repository contains the code and documentation for the final project of the CPE232 course at King Mongkut's University of Technology Thonburi (KMUTT). The project focuses on forecasting global temperature anomalies using **ARIMA** and **SARIMA** models.

## Project Overview

Global temperature anomalies refer to deviations in temperature from historical averages. Understanding these anomalies is essential for analyzing climate variability and making informed predictions about future climate trends. 

This project uses time series data from NOAA, spanning from the year 2000 to 2024 (monthly), to build ARIMA and SARIMA models to forecast temperature anomalies. The dataset consists of three categories:
- Global Land and Ocean
- Global Land Only
- Global Ocean Only

By employing ARIMA and SARIMA models, the goal of this project is to predict future temperature trends, comparing the performance and accuracy of both models.

## Models

### ARIMA (Auto-regressive Integrated Moving Average)
ARIMA is a widely used statistical analysis model for time series data. It combines autoregression (AR), differencing (I), and moving average (MA) to predict future values based on past data.

### SARIMA (Seasonal Auto-regressive Integrated Moving Average)
SARIMA builds upon ARIMA by adding parameters to handle seasonality in the data. This makes SARIMA more effective for datasets with periodic patterns, such as global temperature anomalies.

## Results
- **ARIMA**: Initially, the ARIMA model indicated a downward trend, contrary to our expectations of rising temperatures. This discrepancy led us to explore the seasonality aspect, which the ARIMA model didn't handle effectively.
- **SARIMA**: Incorporating seasonality through SARIMA improved forecast accuracy, as it captured both non-seasonal and seasonal patterns in the data. The SARIMA model showed a more efficient and accurate forecasting result compared to ARIMA.

## Dataset
The temperature anomaly time series datasets were sourced from NOAA’s Climate at a Glance service. The dataset contains:
- Monthly global land and ocean temperature anomaly data from 2000 to 2024
- 288 attributes, making it sufficient for training the forecasting models

### Data Source:
- [NOAA Global Time Series](https://www.ncei.noaa.gov/access/monitoring/climate-at-a-glance/global/time-series)

## Libraries Used
- `statsmodels` (for ARIMA and SARIMA model creation)
- `pmdarima` (for Auto-ARIMA)
- Other essential Python libraries: `pandas`, `numpy`, `matplotlib`, etc.

## Model Selection Process
- **Augmented Dickey-Fuller Test**: Used to test for stationarity in the dataset
- **Auto-ARIMA**: Automatically selected the best parameters for the ARIMA and SARIMA models
- **Rolling Statistical Test**: Applied rolling mean and standard deviation to explore trends in the time series data

## Key Features of the Models

| Feature | ARIMA | SARIMA |
|---------|-------|--------|
| Seasonality Handling | No | Yes |
| Components | AR + I + MA | AR + I + MA + Seasonal |
| Stationarity | Requires differencing | Can handle both seasonal and non-seasonal stationarity |
| Use Cases | Suitable for non-seasonal time series | Ideal for time series with seasonal patterns |

## Conclusion
The SARIMA model proved to be more effective in capturing the upward trend of temperature anomalies due to its ability to model seasonality. However, adjustments to model settings and the inclusion of more extensive data could further improve the forecast accuracy.

## FAQs
- **Why forecast global temperature anomalies?**  
  Forecasting temperature anomalies provides insight into long-term climate trends, essential for understanding climate change and informing policy decisions.
  
- **How do ARIMA and SARIMA differ?**  
  ARIMA is suited for non-seasonal time series, while SARIMA incorporates seasonal patterns, making it more suitable for data with periodic fluctuations.

- **What are the limitations of ARIMA/SARIMA?**  
  Both models are statistical and may not capture complex climate factors like solar activity or volcanic eruptions. Their accuracy decreases over long-term forecasts.

## References
- Hyndman, R. J., & Athanasopoulos, G. (2018). *Forecasting: Principles and Practice*. OTexts.
- Monitoring.Info@noaa.gov. Global Time Series | Climate at a Glance | National Centers for Environmental Information (NCEI).
- Peixeiro, M. (2022). *Time Series Forecasting in Python*.
- Panda, A., et al. (2021). Forecasting Temperature Anomalies of Planet Earth: A Comparative Analysis of AI Models.
