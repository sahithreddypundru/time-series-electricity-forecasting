# time-series-electricity-forecasting

Forecasting Weekly German Electricity Demand
Overview

This repository contains the implementation of a time series forecasting project completed for the Advanced Research Topics module as part of the MSc Data Science programme at the University of Hertfordshire.

The project investigates several forecasting techniques for predicting weekly German electricity demand and compares traditional statistical models with machine learning and deep learning approaches.

Objectives

The main objectives of this project are to:

Analyse historical German electricity demand.
Develop benchmark forecasting models.
Build SARIMA and SARIMAX forecasting models.
Develop a feature-based machine learning model.
Train an LSTM neural network using hourly electricity demand.
Compare model performance using common forecasting metrics.
Dataset
Electricity Demand
Source: Open Power System Data (OPSD)
Country: Germany
Original frequency: Hourly
Study period: January 2015 – September 2020
Weather Data
Source: Open-Meteo Archive API
Location: Berlin
Variables:
Weekly Mean Temperature
Heating Degree Days (HDD)
Cooling Degree Days (CDD)
Forecasting Models

The following forecasting methods were implemented:

Mean Forecast
Naive Forecast
Drift Forecast
Seasonal Naive Forecast
SARIMA
SARIMAX
HistGradientBoostingRegressor
Long Short-Term Memory (LSTM)
Feature Engineering

The machine learning model uses:

Lag Features
Rolling Mean
Rolling Standard Deviation
Calendar Features
Fourier Features

A Random Forest model was additionally used to analyse feature importance. It was not used for forecasting.

Evaluation Metrics

Model performance was evaluated using:

Mean Absolute Error (MAE)
Root Mean Squared Error (RMSE)
Mean Absolute Scaled Error (MASE)
Results
Model	MAE	RMSE
Mean	3.789	4.397
Naive	3.783	4.459
Drift	4.340	5.118
Seasonal Naive	2.063	2.672
SARIMA	2.134	2.730
SARIMAX	2.745	3.485
HistGradientBoosting	1.953	2.661
LSTM	0.693	0.908
Summary
Seasonal Naive was the strongest benchmark model.
SARIMA improved upon the benchmark methods.
Adding weather variables through SARIMAX did not improve forecasting accuracy.
The HistGradientBoosting model produced the best performance among the weekly forecasting models.
The LSTM model achieved the lowest prediction errors overall.
