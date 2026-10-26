# USD/INR Exchange Rate Forecasting Using Machine Learning

## Overview

An undergraduate economics and machine learning project that forecasts the next available USD/INR exchange-rate observation using historical Reserve Bank of India data.

The project demonstrates data cleaning, exploratory analysis, feature engineering, model training, chronological evaluation, and comparison against a simple benchmark.

## Research Question

Can a Random Forest Regressor forecast the next USD/INR observation more accurately than a naive model that predicts no change from the latest observed rate?

## Data

- Source: Reserve Bank of India, Database on Indian Economy (DBIE)
- Dataset: Daily interbank forex rates, USD vis-a-vis INR
- Data used: 8 August 2000 to 30 June 2026
- Target: RBI Reference Rate
- Source link: https://dbie.rbihub.in/statistics?table=financial_markets.r691_daily_interbank_forex_rates_usd_vis_a_vis_inr

## Methods

- Python, pandas and NumPy for data preparation
- Matplotlib for visualisation
- scikit-learn Random Forest Regressor
- Lagged exchange rates and 5- and 20-observation moving averages
- Chronological training and test split
- Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE)

## Holdout Evaluation

| Model | MAE (INR) | RMSE (INR) |
|---|---:|---:|
| Random Forest | 2.8030 | 3.9650 |
| Naive baseline | 0.2171 | 0.3074 |

Lower values indicate better performance. In this holdout evaluation, the naive baseline performed better than the Random Forest. The results show why machine learning forecasts should be compared against simple benchmarks.

## How to Run

1. Open the notebook in Google Colab.
2. Download the RBI CSV dataset using the source link above.
3. Upload the CSV when prompted by the notebook.
4. Run the cells in order.
5. Review the forecast plots, evaluation metrics, and limitations.

## Limitations

- The model uses historical exchange rates and does not include macroeconomic fundamentals.
- Results are based on a single chronological holdout period.
- Random Forest has limited ability to extrapolate beyond the training target range.
- The dataset ends on 30 June 2026 and does not provide a current market quote.
- Forecasts are experimental and are not financial advice.

## Skills Demonstrated

Python | Data Cleaning | Exploratory Data Analysis | Feature Engineering | Scikit-learn | Random Forest | Forecast Evaluation | Economic Interpretation

## Author

Undergraduate economics portfolio project.
