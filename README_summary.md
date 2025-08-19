# Electricity Demand Forecasting (XGBoost-ready)

**Goal:** Forecast hourly electricity demand using weather and calendar features with robust time-series validation.

**Pipeline:** EDA → lag & rolling features → time-based split → models (Linear, RandomForest, XGBoost/GBR) → TimeSeriesSplit CV → plots & feature importances.


**Best Test Model (by RMSE):** XGBoost


**Test metrics:**

                Model        MAE        RMSE       R2
              XGBoost  99.265129  147.249364 0.989142
        Random Forest 125.607480  176.865509 0.984335
    Linear Regression 396.127869  506.487662 0.871536
Naive Lag-24 Baseline 993.752978 1335.696712 0.106571


**TimeSeriesSplit CV (MAE):**

            Model  CV_MAE_Mean  CV_MAE_Std
Linear Regression   424.624228   32.100612
    Random Forest   130.849219   10.769782
          XGBoost   111.985985   26.491897