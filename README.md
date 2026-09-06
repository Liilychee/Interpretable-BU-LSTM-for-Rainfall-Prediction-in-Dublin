# Short-Term Regional Precipitation Forecasting over Dublin

This repository contains the code, processed data, trained model files, and evaluation results associated with the study:

**Short-Term Regional Precipitation Forecasting over Dublin Using ERA5 Reanalysis: Robustness, Probabilistic Reliability, and Predictor Attribution**

## Contents

- `code/` – data processing, model training, evaluation, SHAP analysis, and figure generation
- `data/` – processed Dublin regional ERA5 dataset used in the experiments
- `models/` – saved trained model weights
- `results/` – point-forecast, probabilistic, bootstrap, SHAP, threshold, and ablation results

## Experimental setting

- ERA5 reanalysis data, 2004–2021
- 6-hourly observations
- Dublin regional mean precipitation forecasting
- Six-step input window
- 6-hour-ahead prediction

## Main analyses

- Deterministic and probabilistic forecasting
- Five-seed performance stability analysis
- Rainfall-regime and threshold-based evaluation
- Probabilistic reliability using NLL, CRPS, prediction-interval coverage, and interval width
- SHAP-based predictor attribution
- Feature-ablation analysis
