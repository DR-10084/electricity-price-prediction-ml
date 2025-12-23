


## Problem
Electricity prices vary hourly in deregulated markets, affecting consumers and generators.

## Solution
This project uses a Random Forest ML model to predict day-ahead electricity prices using load and weather data.

## Why it matters
Accurate price prediction helps in optimal energy usage and market planning.


# Electricity Price Prediction using Machine Learning

This project implements a **Random Forest Regression model** to predict 
**hourly electricity prices** using a combination of **time-based features, 
weather data, load forecast, and power generation data**.

The work focuses on understanding how different factors influence electricity 
prices in a **deregulated electricity market**.


---

## Dataset

This project uses **publicly available datasets from Kaggle**, including:

- Electricity generation data
- Weather data for multiple cities
- Load forecast information
- Actual electricity prices

Two datasets are merged using timestamp alignment:
- Generation dataset (`final_project.generation.csv`)
- Weather dataset (`final_project.weathers.csv`)

Unnecessary weather and generation columns are removed during preprocessing.

---

## Feature Engineering

The following features are used for model training:

### Time-based features
- Hour of the day
- Day of the week
- Month

### System & market features
- Total load forecast
- Solar generation
- Nuclear generation

### Weather & location features
- Temperature
- Weather condition (categorical)
- City name (categorical)

Categorical features (`city_name`, `weather_main`) are encoded using 
**One-Hot Encoding** with a `ColumnTransformer`.

---

## Model Used

- **Algorithm:** Random Forest Regressor
- **Library:** Scikit-learn
- **Train–Test Split:** 80% training, 20% testing
- **Number of Trees:** 100

The model is trained to predict the **actual electricity price**.

---

## Model Evaluation

The model performance is evaluated using:
- **Mean Squared Error (MSE)**
- **R² Score**

Additionally, the following visual analyses are included:
- Average electricity price by **month**
- Average electricity price by **hour**
- **Actual vs Predicted** price comparison
- **Feature importance** analysis from Random Forest

---

## User Input Based Prediction

The project also supports **manual user input** for prediction.

Users can input:
- Day of week
- Hour
- Month
- Load forecast
- Temperature
- Weather condition
- City name
- Solar and nuclear generation values

The trained model then predicts the corresponding electricity price.

---

## Tools & Technologies

- Python
- Jupyter Notebook
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn

---

## Results

The Random Forest model captures **non-linear relationships** between 
electricity prices and influencing factors such as demand, weather, and 
generation mix, producing reasonable prediction accuracy.

Feature importance analysis shows the relative impact of different inputs 
on electricity pricing.

---

## Future Scope

- Hyperparameter tuning for improved accuracy
- Real-time electricity price prediction
- Deployment of the trained model on **FPGA for faster inference**
- Integration with live weather and load forecast data

---

## Author

Diksha Ratha  
B.Tech Electrical & Electronics Engineering  
NIT Uttarakhand
