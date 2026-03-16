# Data directory

This directory holds JSON and image assets for the website.

## Pipeline outputs (pl-predictor)

If you run the pl-predictor model pipeline, it should produce:

1. **evaluation.json** – Overwrite this file with metrics from your evaluation script. Expected structure:
   ```json
   {
     "roc_auc": 0.72,
     "brier_score": 0.19,
     "log_loss": 0.98,
     "precision": {"home": 0.55, "draw": 0.25, "away": 0.52},
     "recall": {"home": 0.58, "draw": 0.22, "away": 0.50},
     "gambling": {
       "flat_roi_pct": 5.2,
       "kelly_pnl": 12.3,
       "sharpe_ratio": 0.45,
       "test_seasons": "2022/23–2024/25"
     }
   }
   ```

2. **calibration.png** – Calibration plot (predicted vs observed).

3. **shap_summary.png** – SHAP summary plot.

Copy these from your pl-predictor `output/` directory into this `data/` folder so the project paper and betting page can display them.
