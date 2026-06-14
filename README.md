# Renewable Energy Intelligence

Renewable energy analytics and forecasting using Python, data science, and machine learning.

## Project Overview

This project investigates the relationship between weather conditions, solar irradiance, and temporal factors on renewable energy production. Using exploratory data analysis (EDA) and machine learning techniques, the project identifies the key drivers of energy generation and develops predictive models capable of forecasting renewable energy output.

The objective is to understand how environmental conditions influence energy production and to evaluate the effectiveness of different machine learning algorithms for renewable energy forecasting.

---

## Dataset

The dataset contains:

* 196,776 observations
* 17 variables
* Weather measurements
* Solar irradiance information (GHI)
* Sunlight-related variables
* Renewable energy production data

Key variables include:

* GHI (Global Horizontal Irradiance)
* Temperature
* Humidity
* Cloud Cover
* Wind Speed
* Rainfall
* Snowfall
* Day Length
* Sunlight Time
* Energy Production (Target Variable)

---

## Exploratory Data Analysis

The exploratory analysis examined the impact of weather and temporal variables on energy production.

### Key Findings

* Approximately 51% of observations have zero energy production.
* Energy production follows a clear daily cycle, with peak generation occurring around midday.
* Energy production exhibits strong seasonal patterns, with summer months producing substantially more energy than winter months.
* Cloud cover negatively impacts energy generation.
* Humidity exhibits a strong negative relationship with energy production.
* Temperature is positively associated with energy production.
* GHI shows the strongest relationship with energy production and is the most influential predictor.

---

## Machine Learning Models

Three machine learning models were developed and evaluated:

1. Linear Regression
2. Random Forest Regressor
3. XGBoost Regressor

### Model Performance

| Model             |    MAE |   RMSE |     R² |
| ----------------- | -----: | -----: | -----: |
| Linear Regression | 224.02 | 396.71 | 0.8572 |
| Random Forest     | 106.02 | 264.56 | 0.9365 |
| XGBoost           | 115.89 | 276.78 | 0.9305 |

### Best Model

The Random Forest model achieved the best overall performance:

* R² = 0.9365
* MAE = 106.02 Wh
* RMSE = 264.56 Wh

This indicates that the model successfully explains approximately 94% of the variation in renewable energy production.

---

## Feature Importance Analysis

Feature importance analysis from the Random Forest model revealed that:

* GHI contributes approximately 85.8% of total predictive importance.
* Day Length is the second most important predictor.
* Most remaining weather variables provide comparatively smaller contributions.

These results confirm that solar irradiance is the dominant driver of renewable energy generation.

---

## Repository Structure

```text
renewable-energy-intelligence/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   └── 01_data_understanding.ipynb
│
├── outputs/
│   ├── figures/
│   └── reports/
│
├── src/
├── tests/
│
├── README.md
└── LICENSE
```

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-Learn
* XGBoost
* Jupyter Notebook
* Git
* GitHub

---

## Conclusion

This project demonstrates that renewable energy production can be accurately predicted using weather and temporal variables. Among the evaluated models, Random Forest achieved the highest predictive performance with an R² score of 0.9365. Feature importance analysis identified GHI (solar irradiance) as the dominant factor influencing renewable energy generation.

---

## Future Improvements

* Hyperparameter tuning
* Cross-validation
* Additional forecasting models
* Automated prediction pipeline
* Deployment as a web application
