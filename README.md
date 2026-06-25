# 🚦 Gridlock Hackathon 2.0
### AI-Powered Traffic Demand Forecasting for Bengaluru

An end-to-end Machine Learning solution developed for **Flipkart Gridlock Hackathon 2.0** in collaboration with **Flipkart × Bengaluru Traffic Police**.

The project leverages historical traffic and geospatial data to forecast traffic demand across Bengaluru, enabling smarter traffic management, congestion reduction, and data-driven urban planning.

## Problem Statement

Rapid urbanization and increasing vehicle density have made traffic congestion one of Bengaluru's most pressing challenges.

The objective of this project is to predict future traffic demand using historical traffic patterns, temporal information, and geospatial features. Accurate forecasting can help authorities:

- Anticipate congestion hotspots
- Optimize traffic signal timings
- Improve route planning
- Enhance emergency response management
- Support smart-city initiatives

## Project Objectives

- Forecast traffic demand for different regions of Bengaluru
- Extract meaningful features from spatial and temporal data
- Build a robust machine learning model for prediction
- Optimize model performance using hyperparameter tuning
- Generate predictions for unseen test data

## Dataset Overview

The dataset contains:

- Traffic demand observations
- Geographical information encoded as Geohashes
- Timestamp information
- Additional traffic-related attributes

### Key Features

| Feature Type | Description |
|-------------|-------------|
| Temporal Features | Hour, Day, Month, Weekday |
| Geospatial Features | Latitude, Longitude (decoded from Geohash) |
| Traffic Features | Historical traffic demand indicators |

---

## Methodology

### 1. Data Preprocessing

- Missing value handling
- Data cleaning
- Feature transformation

### 2. Geospatial Feature Engineering

Geohashes were decoded into:

- Latitude
- Longitude

to provide meaningful geographical coordinates to the model.

### 3. Temporal Feature Engineering

Extracted:

- Hour of Day
- Day of Week
- Month
- Weekend Indicator

from timestamp columns.

### 4. Hyperparameter Optimization

Used **Optuna** to automatically search for the best hyperparameter combinations for the model.

### 5. Model Training

Implemented:

- **XGBoost Regressor**

to learn traffic demand patterns from historical observations.

### 6. Prediction Generation

The trained model was used to generate predictions on the test dataset and create the final submission file.


## Machine Learning Pipeline

```text
Raw Data
    │
    ▼
Data Cleaning
    │
    ▼
Feature Engineering
    │
    ├── Geohash Decoding
    └── Temporal Features
    │
    ▼
Train-Test Split
    │
    ▼
Optuna Hyperparameter Tuning
    │
    ▼
XGBoost Model Training
    │
    ▼
Prediction Generation
    │
    ▼
submission.csv
```


## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-Learn
- XGBoost
- Optuna
- PyGeoHash
- Jupyter Notebook

---

## Repository Structure

```text
Gridlock-Hackathon-2.0/
│
├── model.ipynb              # Model development notebook
├── submission.csv           # Final predictions
├── README.md
├── requirements.txt
└── .gitignore
```


## How to Run

### Clone Repository

```bash
git clone https://github.com/NishiVatsha/Gridlock-Hackathon-2.0.git
cd Gridlock-Hackathon-2.0
```

### Install Dependencies

```bash
### Install Dependencies

```bash
pip install pandas numpy scikit-learn xgboost optuna pygeohash jupyter
```
```

### Launch Notebook

```bash
jupyter notebook
```

Open:

```text
model.ipynb
```

and run all cells.

## Results

The final solution utilizes an optimized XGBoost model tuned using Optuna to improve predictive performance on Bengaluru traffic demand forecasting.

Performance was evaluated using the competition's evaluation metric.

## Future Improvements

- Incorporate weather information
- Integrate real-time traffic feeds
- Experiment with LightGBM and CatBoost
- Deploy as a web application
- Build live congestion prediction dashboards

## Author

**Nishi Vatsha**

B.Tech Computer Science Engineering (Data Science)  
Mody University of Science and Technology


## Hackathon

Developed as part of **Flipkart Gridlock Hackathon 2.0**, focused on building AI-driven solutions for urban traffic intelligence and smart mobility.
