# 🚕 NYC Yellow Taxi Trip Duration Prediction
### Geospatial Data Engineering & Machine Learning

An end-to-end geospatial machine learning pipeline for predicting NYC Yellow Taxi trip duration using large-scale transportation data.

This project combines **data engineering, geospatial analytics, feature engineering, and supervised regression modeling** to analyze over **500K+ taxi trips** and identify factors influencing travel time.

---

## 📌 Project Overview

Trip duration prediction is an important problem in transportation analytics and smart mobility systems.

This project processes NYC Yellow Taxi trip records and builds predictive models capable of estimating trip duration using:

- Temporal features
- Spatial relationships
- Route behavior
- Distance transformations
- Geospatial feature engineering

The workflow emphasizes **clean data pipelines, reproducibility, and robust model evaluation**.

---

## 📂 Dataset

**Source:** NYC TLC Yellow Taxi Trip Records (Jan–Mar 2023)

Dataset includes:

- Pickup timestamps
- Dropoff timestamps
- Pickup location IDs
- Dropoff location IDs
- Trip distance
- Fare amount
- Passenger count

Data Format:
- Multi-file Parquet datasets
- ~145 MB raw data
- Millions of transportation records

---

## ⚙️ Technologies Used

### Programming
- Python

### Data Engineering
- Pandas
- NumPy
- scikit-learn Pipelines
- ColumnTransformer

### Geospatial Analytics
- GeoPandas
- Shapefile Processing
- Coordinate Reference Systems (CRS)
- Haversine Distance

### Machine Learning
- Ridge Regression
- Lasso Regression
- ElasticNet
- Huber Regression

### Visualization
- Matplotlib
- Seaborn

---

# 🏗 Project Architecture

```text
Raw Parquet Files
        ↓
Data Loading
        ↓
Data Cleaning
        ↓
Feature Engineering
        ↓
Preprocessing Pipeline
        ↓
Model Training
        ↓
Evaluation
        ↓
Error Analysis
```

---

# 🔍 Workflow

## 1. Data Loading & Exploratory Data Analysis

- Loaded multi-source Parquet datasets
- Generated target variable (`trip_duration`)
- Filtered unrealistic trips
- Analyzed distributions and missing values

---

## 2. Feature Engineering

Created:

### Temporal Features
- Hour of day
- Day of week
- Weekend indicator
- Rush hour indicator

### Spatial Features
- Haversine distance
- Zone route frequency
- Pickup frequency
- Dropoff frequency
- Same-zone detection

### Distance Features
- Log distance
- Fare per mile
- Distance ratio

---

## 3. Data Preprocessing

Implemented:

- `Pipeline`
- `ColumnTransformer`
- Median imputation
- Categorical imputation
- Standard scaling
- One-hot encoding

---

## 4. Model Training

Regression models evaluated:

| Model | Purpose |
|-------|--------|
| Ridge | L2 Regularization |
| Lasso | Feature Selection |
| ElasticNet | Hybrid Regularization |
| Huber | Outlier Robust |

Training Split:
- 60% Train
- 20% Validation
- 20% Test

---

## 📈 Model Evaluation

Performance metrics:

- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- R² Score

Additional analysis:

- Learning Curves
- Residual Diagnostics
- Bias–Variance Analysis
- Systematic Error Analysis

---

## 🌍 Geospatial Engineering Components

This project includes practical geospatial workflows:

✔ Coordinate Reference System (CRS) transformation  
✔ Shapefile processing  
✔ Spatial feature generation  
✔ Distance approximation using Haversine formula  
✔ Zone-based transportation analytics  

---

## 🚀 Key Outcomes

- Built a scalable geospatial preprocessing workflow
- Improved transportation feature representation
- Compared multiple regression loss functions
- Investigated outlier effects in urban mobility data
- Generated reproducible ML pipelines

---

## 📁 Repository Structure

```text
├── data/
├── notebooks/
├── models/
├── visuals/
├── src/
├── README.md
└── requirements.txt
```

---

## 💡 Future Improvements

- Add Airflow orchestration
- Integrate dbt transformations
- Experiment with XGBoost
- Incorporate traffic and weather data
- Extend to real geospatial databases (PostGIS)

---

## 👩‍💻 Author

**Anne Carol G. Jonson**  
BS Computer Science – Data Science Specialization  
University of Santo Tomas
