# Time Series Analysis for Air Passenger Demand Prediction

![Time Series](https://www.analyticsvidhya.com/wp-content/uploads/2018/09/major-3-750x420.jpg)

## Project Overview

This project focuses on building a predictive model to predict or forecast the demand (passenger traffic) in airplanes using Time Series Forecasting models. The primary feature variable is the Month, and the target variable is the number of Passengers.

## Table of Contents

- [Introduction](#introduction)
- [Models](#models)
  - [Additive Model](#additive-model)
  - [Multiplicative Model](#multiplicative-model)
- [Data Stationarity](#data-stationarity)
  - [Rolling Statistics Test](#rolling-statistics-test)
  - [ADF (Augmented Dickey-Fuller) Test](#adf-augmented-dickey-fuller-test)
- [Results](#results)
- [Conclusion](#conclusion)
- [References](#references)

## Introduction

Time Series forecasting involves using statistical models to predict future values based on past data. For this project, we aim to predict the number of airplane passengers in the upcoming months.

## Models

### Additive Model

An additive model suggests that the components are added together:

\[ Y(t) = T(t) + C(t) + S(t) + R(t) \]

Where:
- \( T(t) \) is the trend component
- \( C(t) \) is the cyclic component
- \( S(t) \) is the seasonal component
- \( R(t) \) represents random fluctuations (residuals)

### Multiplicative Model

A multiplicative model suggests that the components are multiplied together:

\[ Y(t) = T(t) \times C(t) \times S(t) \times R(t) \]

## Data Stationarity

Before performing time-series analysis, it's crucial to check if the data is stationary.

### Rolling Statistics Test

A rolling analysis assesses model stability over time. By creating a rolling window, calculations are performed on the data within this window, which rolls through the data.

![Rolling Statistics](https://miro.medium.com/v2/resize:fit:1000/format:webp/1*udlhGz7lqyDMLX4G97Ghvw.png)

### ADF (Augmented Dickey-Fuller) Test

This test helps determine if the data is non-stationary.

- **Null Hypothesis**: Data is non-stationary
- **Test Statistic**: The more negative, the more likely the data is stationary
- **p-value**: If < 0.05, reject null hypothesis and conclude data is stationary

Example:
- Test Statistic: -11.638
- p-value: < 0.05 (Reject null hypothesis, data is stationary)

## Results

- **Rolling Statistics Test**: Demonstrates model stability over time.
- **ADF Test**: Confirms data stationarity with a test statistic of -11.638 and a p-value < 0.05.

## Conclusion

The project successfully demonstrated the process of time-series analysis and forecasting for airplane passenger demand. By ensuring data stationarity and applying appropriate models, accurate predictions for future passenger traffic were achieved.

## References

- [Time Series Analysis](https://www.analyticsvidhya.com/blog/2021/04/statistics-for-time-series-analysis/)
- [ADF Test Documentation](https://www.statsmodels.org/stable/generated/statsmodels.tsa.stattools.adfuller.html)
