
# Short-Term Regional Precipitation Forecasting over Dublin

This repository contains the code, processed data, trained model weights, and experimental results for short-term precipitation forecasting over Dublin using ERA5 reanalysis data.

The project evaluates deterministic and probabilistic machine learning models, with a focus on forecasting performance, robustness, uncertainty estimation, and meteorological feature analysis.

## Dataset

- **Data source:** ERA5 Reanalysis
- **Study area:** Dublin, Ireland
- **Period:** 2004–2021
- **Temporal resolution:** 6 hours
- **Input sequence:** 6 time steps
- **Forecast horizon:** 6 hours ahead
- **Prediction target:** Regional mean precipitation

ERA5 data are provided by the Copernicus Climate Change Service (C3S).

[ERA5 Dataset](https://cds.climate.copernicus.eu/datasets/reanalysis-era5-single-levels)

## Models

The experiments include:

- Persistence and climatology baselines
- XGBoost
- Transformer
- BiLSTM
- BiLSTM-Attention
- BU-LSTM
- BU-LSTM-Attention
- Probabilistic recurrent models

## Evaluation

The project includes the following analyses:

- **Deterministic forecasting:** RMSE, MAE, and R²
- **Probabilistic forecasting:** NLL, CRPS, and prediction interval coverage
- **Robustness:** Evaluation across five random seeds
- **Rainfall regimes:** Performance under different precipitation intensities
- **Extreme events:** Threshold-based evaluation
- **Model comparison:** Bootstrap analysis
- **Interpretability:** SHAP-based feature attribution
- **Feature analysis:** Feature-ablation experiments

## Repository Structure

```text
├── code/
│   └── Interpretable_analysis.ipynb
├── data/
│   └── dublin_regional_2004_2021.csv
├── models/
│   ├── bilstm_attention_final_seed42.weights.h5
│   └── proposed_model_seed42.weights.h5
├── results/
│   ├── final_5seed_point.csv
│   ├── final_5seed_probabilistic.csv
│   ├── final_single_run_point.csv
│   ├── final_single_run_probabilistic.csv
│   ├── final_global_shap_importance.csv
│   ├── final_thresholds.csv
│   └── ...
└── README.md
```

## Code

The main experimental notebook is available in:

[`code/Interpretable_analysis.ipynb`](code/Interpretable_analysis.ipynb)

It contains implementations for data processing, model training, evaluation, and interpretability analysis.

## Results

The `results/` directory contains:

- Model predictions and performance metrics
- Multi-seed evaluation results
- Probabilistic forecasting metrics
- Rainfall-regime and threshold-based evaluations
- Bootstrap comparisons
- SHAP attribution results
- Feature-ablation results

Trained model weights are available in the `models/` directory.
