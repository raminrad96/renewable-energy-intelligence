# Renewable Energy Intelligence: Energy Production Forecasting Using Machine Learning

## 1. Introduction

Renewable energy production relies largely on meteorological conditions and environment. It becomes crucial to comprehend such dependencies to enhance the accuracy of predictions as well as ensure efficient energy management.

The proposed project aims to examine dependencies between weather parameters, solar radiation, and time-related data and renewable energy production. The goal of the project is to find critical factors affecting the process under analysis and build accurate prediction models based on machine learning.

---

## 2. Dataset Description

The dataset contains 196,776 observations and 17 variables related to weather conditions, sunlight measurements, and energy generation.

Key variables include:

* Energy delta [Wh] (Target Variable)
* GHI (Global Horizontal Irradiance)
* Temperature
* Humidity
* Wind Speed
* Cloud Cover
* Rainfall
* Snowfall
* Day Length
* Sunlight Time
* Hour
* Month

The dataset contains no missing values and provides sufficient observations for machine learning analysis.

---

## 3. Exploratory Data Analysis

Several analyses were conducted to understand the factors affecting renewable energy generation.

### Daily Patterns

Energy production follows a clear daily cycle. Production is near zero during nighttime hours and peaks around midday when solar exposure is highest.

### Seasonal Patterns

Energy generation exhibits strong seasonality. Summer months produce significantly more energy than winter months due to longer daylight periods and higher solar irradiance.

### Weather Effects

The analysis revealed several important relationships:

* GHI has a strong positive relationship with energy production.
* Humidity has a strong negative relationship with energy production.
* Cloud cover negatively affects energy generation.
* Temperature is positively associated with energy production.

### Correlation Analysis

GHI demonstrated the strongest correlation with energy production (0.915), indicating its importance as a predictive feature.

---

## 4. Machine Learning Models

Three machine learning models were developed and evaluated:

### Linear Regression

Linear Regression was used as a baseline model to establish a performance benchmark.

### Random Forest Regressor

Random Forest was used to capture complex and non-linear relationships between weather variables and energy production.

### XGBoost Regressor

XGBoost was implemented as an advanced gradient boosting model to compare performance against Random Forest.

---

## 5. Results

### Model Performance

| Model             |    MAE |   RMSE |     R² |
| ----------------- | -----: | -----: | -----: |
| Linear Regression | 224.02 | 396.71 | 0.8572 |
| Random Forest     | 106.02 | 264.56 | 0.9365 |
| XGBoost           | 115.89 | 276.78 | 0.9305 |

### Best Model

Random Forest achieved the highest predictive performance with:

* R² = 0.9365
* MAE = 106.02 Wh
* RMSE = 264.56 Wh

The model successfully explained approximately 94% of the variation in renewable energy production.

### Feature Importance

Feature importance analysis revealed that GHI is the dominant predictor, contributing approximately 85.8% of total predictive importance.

Day Length was identified as the second most important feature, while the remaining weather variables contributed smaller amounts of predictive information.

---

## 6. Conclusion

Renewable energy generation can be successfully predicted through the use of environmental and temporal features.

It was determined via exploratory analysis that solar irradiation, humidity, temperature, and seasonality play a key role in energy generation. The machine learning experiments indicated that Random Forest algorithm performed better than other models.

Therefore, this study proved once again that solar irradiation is the most influential factor of renewable energy generation and energy output can be forecasted through machine learning approaches.

Possible directions for improvement may involve hyperparameter tuning, validation process, and the implementation of the prediction application.