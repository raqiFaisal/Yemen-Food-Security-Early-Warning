# Yemen Food Security Early Warning

A leakage-aware, time-ordered machine-learning benchmark for the `target_ipc4` label in `YEM_JMR_data.csv`.

## Files
- `Yemen_Food_Security_Early_Warning_FINAL.ipynb`: main notebook.
- `requirements.txt`: Python dependencies.
- `.gitignore`: excludes generated models, outputs, and sensitive/local data.
- Runtime-generated outputs: `model_comparison_validation.csv`, `threshold_selection_validation.csv`, `final_test_metrics.csv`, `test_predictions.csv`, `feature_importance_validation.csv`, and `run_metadata.json`.

## Run on Kaggle
1. Create a Kaggle Notebook.
2. Use **Add Input** to attach the dataset containing `YEM_JMR_data.csv`.
3. Upload/import this notebook and run all cells.
4. Outputs are written to `/kaggle/working/`; download them from the notebook's Output panel.

## Run locally
Place `YEM_JMR_data.csv` beside the notebook and install dependencies:
```bash
python -m pip install -r requirements.txt
jupyter notebook Yemen_Food_Security_Early_Warning_FINAL.ipynb
```

## Scientific caution
The dataset has labels for only a subset of rows/months and does not provide explicit feature publication timestamps or an unambiguous forecast horizon. The notebook therefore evaluates a chronological retrospective classification task. It does **not** claim a validated operational early-warning system. `predicted_prob`, IPC-adjacent target fields, and `estimated_pop_at_risk` are excluded from model features. Several price/exchange “original” and “volatility_original” columns are exact duplicates; redundant copies are removed.

## GitHub
Do not commit confidential or restricted raw data. Commit the notebook, documentation, and dependency files; add generated outputs only if appropriate and documented. Review the data provider's license and sharing rules before publishing.
