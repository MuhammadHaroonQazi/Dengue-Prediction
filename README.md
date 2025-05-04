# Dengue Case Prediction using XGBoost
This project uses machine learning to predict weekly dengue cases in two cities — San Juan and Iquitos — based on environmental and weather-related features.

The best-performing model (XGBoost Regressor) achieved:
- **San Juan MAE:** 5.29
- **Iquitos MAE:** 1.68
The dataset was provided in three CSV files:
- `dengue_features_train.csv` — training features
- `dengue_labels_train.csv` — corresponding dengue case counts
- `dengue_features_test.csv` — features for prediction

Each row represents one week, with climate features like:
- NDVI (vegetation)
- Temperature
- Humidity
- Precipitation
The following additional features were created:
- Lag features (`lag_1_total_cases`, `lag_2_total_cases`)
- Rolling mean and std of total cases
- Temperature difference (`temp_diff`)
Tested models:
- Random Forest Regressor
- Gradient Boosting Regressor
- LightGBM
- ✅ XGBoost Regressor (best model)

Evaluation Metric: **Mean Absolute Error (MAE)**

Final Results:
| Model       | San Juan MAE | Iquitos MAE |
|-------------|--------------|-------------|
| RandomForest| 7.99         | 4.44        |
| LightGBM    | ~7.3         | ~4.0        |
| **XGBoost** | **5.29**     | **1.68**    |
1. Clone the repo
2. Run `XGBoost_Dengue_Training_Only.ipynb` in Jupyter
3. The final predictions will be saved to `dengue_predictions.csv`
- pandas
- numpy
- xgboost
- scikit-learn
- matplotlib

