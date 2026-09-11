# Systematic Weather Forecasting & Polymarket Research

## Objective

Build a data-driven weather forecasting system and investigate whether forecast uncertainty and prediction-market contract mechanics can be translated into systematic probability estimates.

## Weather Forecasting System

The forecasting project used historical weather observations and engineered time-series features, including lagged and rolling information, to predict future temperature outcomes.

Research components included:

- historical data ingestion and cleaning
- lag and rolling feature engineering
- multiple machine-learning model families
- model comparison
- ensemble forecasts
- walk-forward validation
- uncertainty-aware forecasts

The project later explored ensemble weather forecasts rather than relying only on a single deterministic prediction, with the goal of estimating both a central forecast and the distribution of plausible outcomes.

## Polymarket Temperature Research

The forecasting work was extended to Cape Town temperature prediction markets on Polymarket.

A key research step was studying the exact resolution mechanism rather than assuming the contract behaved like a generic temperature bet. The work investigated how Weather Underground reports the daily maximum and how a whole-Fahrenheit observation is converted into Celsius for market resolution.

That conversion/rounding mechanism was treated as a potential source of pricing disagreement: a forecast distribution can be translated through the same resolution rules used by the contract and then compared with market-implied probabilities.

## Quantitative Principles

- Forecast distributions matter more than a single point forecast.
- Validation must be chronological.
- Contract resolution mechanics are part of the model.
- Apparent pricing edges must survive realistic uncertainty and validation.
- A model should express probability rather than false certainty.

## Status

The weather forecasting system was completed as a working forecasting project. The prediction-market work remains a research application of those forecasting and probability methods.
