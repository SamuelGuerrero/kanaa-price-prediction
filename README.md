# Kanaa Price Prediction

This repository is organized by training phases to make the workflow clear and repeatable.

## Project Structure
- `database.csv` — dataset (kept at project root)
- `best_xgb_model.pkl` — exported model (kept at project root)
- `01_training/` — EDA + baseline regression
- `02_model_selection/` — initial XGBoost model
- `03_hyperparameter_tuning/` — Grid Search for XGBoost
- `04_kfold_evaluation/` — K-Fold evaluation and model comparison
- `05_export/` — final export notebook to create the `.pkl`
- `06_server/` — Flask server entry point

## Notebooks by Phase
- `01_training/kanaa-price-prediction.ipynb`
- `02_model_selection/kanaa-price-prediction-xgb.ipynb`
- `03_hyperparameter_tuning/kanaa-price-prediction-xgb-gridsearch.ipynb`
- `04_kfold_evaluation/kanaa-price-prediction-xgb-kfold.ipynb`
- `05_export/kanaa-price-prediction-xgb-export.ipynb`

## How to Run
1. Open the notebooks in order to reproduce the full workflow.
2. Ensure `database.csv` is in the project root.
3. When exporting, the model is saved to `best_xgb_model.pkl` in the project root.

## Server
- Entry point: `06_server/main.py`
- Load the model from `../best_xgb_model.pkl` inside the server folder.

## Notes
- All notebooks reference the dataset using `../database.csv` so they work from their phase folder.
- If you retrain and export, the `best_xgb_model.pkl` file will be overwritten.
