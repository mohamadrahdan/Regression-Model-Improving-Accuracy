# Regression Model: Improving Model Accuracy through Feature Engineering

This project demonstrates how feature engineering, data scaling, and evaluation metrics can significantly improve the accuracy of regression models.  
The example dataset focuses on car prices, but the same methodology applies to environmental and geospatial datasets such as predicting NDVI from rainfall or modeling land subsidence based on terrain parameters.

---

## Objective
To explore how data preprocessing, feature optimization, and model evaluation affect regression performance and prediction accuracy.

---

## Dataset Overview
The dataset (originally from CarDekho) includes the following features:

- Present_Price — Current ex-showroom price (in lakhs)  
- Kms_Driven — Kilometers driven by the car  
- Fuel_Type — Type of fuel (Petrol/Diesel/CNG)  
- Seller_Type — Type of seller (Dealer/Individual)  
- Transmission — Transmission type (Manual/Automatic)  
- Owner — Number of previous owners  
- Year — Year of manufacturing  
- Selling_Price — Target variable (price at which the car is sold)

A new feature was created:
Age = 2019 - Year  

Irrelevant columns such as Car_Name and Year were removed.

---

## Preprocessing Steps
- Encoding categorical variables using LabelEncoder (Fuel_Type, Seller_Type, Transmission)  
- Feature engineering: creating a new Age column to represent car depreciation  
- Feature scaling: normalizing numeric features using StandardScaler  
- Train/Test split: 80/20 ratio for model evaluation  
- Model fitting: Linear Regression model using scikit-learn

---

## Key Concepts
- Feature Engineering — creating or selecting meaningful variables (e.g., transforming year into car_age)  
- Scaling — normalizing features to improve model convergence  
- Model Evaluation — using MAE, MSE, RMSE, and R² metrics  
- Visualization — comparing predicted vs. actual prices  
- Model Improvement — refining model through feature analysis and data cleaning

---

## Why It Matters
Although this dataset is automotive, the techniques are universally applicable to real-world problems such as:

- Environmental modeling — predicting vegetation index (NDVI) from rainfall  
- Landslide susceptibility — regression between slope, rainfall, and soil type  
- Climate analysis — modeling temperature or air quality trends  

These regression principles form the foundation of GeoAI and Remote Sensing modeling.

---

## Evaluation Example
| Metric | Example Value |
|--------|----------------|
| MAE | 0.58 |
| MSE | 0.54 |
| RMSE | 0.73 |
| R² Score | 0.97 |


---

## Visualization
![Preview](preview.png)
![Preview](https://www.kaggleusercontent.com/kf/174407173/eyJhbGciOiJkaXIiLCJlbmMiOiJBMTI4Q0JDLUhTMjU2In0..OZnnJ9WpqCiAtNH9opLYQg.ESBSd_hrtvtNn_Dz9Nbp58OQYW-UV9nTME9ZuWWOyVjOFgRok0ti6CBvFl3Ks63dUjhCtQDOPeVmkQzY49sCZVuksZpZ07P30X0m9tkw9ZX4E8eujR_Gsdl26Cp1bVUN5DLhRIB6VzKbaJusjYk89_TpxvAy2lcOYtd_MxTLxkRBGTE21xIPIlQpSABf1ZmbeQMrUG9SY-cHTd65Bt0KZBkXmF__E80wsAgWBw39djJ7r0li0eC9mBhlQ05tJ1_tqjfUsgm_J3sVvzK4dnQuqbRhrXSUfl4W5kz6TmQN0IGbH4vOJQ6EckIS5PowJVqWrD5l5CLwgKwGDs6MtB_cQjb4EWm3XPTszNIqdBdY_lsuCYutitsAprkjXq7auN3gso7rCZlE-Pt_BZ-PLrF2uvXWLctxXv-OWIEw8v2rAk4SMy6NqMA2kXSvrVi2RapaYRi1rlEMIBERa4i7iyQqo21tTYZbgKiHgdjoXIIwcDcehq57LgsHvyMxCiutgmmU-yJoWoOEOn4c4eRQb5xQfX3rjsgIoHHqw3T95eKdjmaEBuB_fn5Gpn8D0jqxpYw7uuwno2y0osS7uFrDrBK8NeFfXPNb1QS_pW5IuKsv1iK1wSV-gT4WPoiJhQcu8ydcooEXEy12B7WDFIC_B-_sEEEas--xfNzsYlUaq1RNVzE.__Rq5bPgBfP6nLCmmE_r0g/__results___files/__results___23_1.png)

---

## Tech Stack
- Python 3.x  
- pandas, numpy  
- scikit-learn  
- matplotlib, seaborn

---

## Run the Notebook
```bash
jupyter notebook "Linear Regression model.ipynb"
