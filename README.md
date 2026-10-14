
## Overview

This repository contains the code, processed ERA5 data, trained model weights, and experimental results associated with the study:

**Short-Term Regional Precipitation Forecasting over Dublin Using ERA5 Reanalysis: Robustness, Probabilistic Reliability, and Predictor Attribution**

**Manuscript status:** Under review.

This study systematically evaluates machine learning and deep learning approaches for 6-hour-ahead regional mean precipitation forecasting over Dublin using 6-hourly ERA5 reanalysis data from 2004 to 2021.

The evaluation includes reference forecasts, XGBoost, Transformer, deterministic BiLSTM architectures, and probabilistic recurrent models. Particular attention is given to multi-seed robustness, rainfall-regime performance, probabilistic reliability, and meteorological predictor attribution.

## Key Findings

- **Predictive performance:** BiLSTM-Attention achieved the lowest mean test RMSE of **0.2429 mm**, closely followed by XGBoost at **0.2439 mm**. Bootstrap analysis showed no clear difference between these models over the full test set or under wet conditions.

- **Heavy rainfall:** XGBoost achieved lower prediction error during heavy rainfall, while event-detection performance deteriorated as precipitation thresholds increased.

- **Probabilistic reliability:** Probabilistic recurrent models achieved approximately nominal 95% prediction interval coverage over the full test set, but substantially underestimated uncertainty for high-intensity rainfall.

- **Predictor attribution:** SHAP analysis identified total cloud cover, meridional wind, surface pressure, and minimum precipitation rate as influential predictors.

- **Feature ablation:** Total cloud cover provided more stable incremental predictive information than maximum precipitation rate, despite the latter's strong correlation with the prediction target.

## Research Contributions

1. A systematic comparison of deterministic and probabilistic forecasting models for regional precipitation prediction.
2. Robustness evaluation across five fixed random seeds, rainfall regimes, and precipitation thresholds.
3. An assessment of uncertainty calibration, highlighting limitations in upper-tail reliability.
4. Complementary SHAP and feature-ablation analyses to investigate meteorological predictor contributions.
