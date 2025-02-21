# New-York-Taxi-Fare-Prediction-using-Machine-Learning
This project aims to predict taxi fares in New York City using machine learning models, primarily Random Forest Regressor, and compares its performance with Multilinear Regression and Decision Tree Regressor


1. Importing Necessary Libraries

pandas, numpy for data manipulation
matplotlib.pyplot, seaborn for data visualization
sklearn modules for machine learning models and evaluation metrics
geopy for calculating geodesic distances between coordinates


2. Loading the Dataset

Dataset loaded from train.csv using pandas.read_csv().
Initial data exploration through .head() and .info() methods.

3. Data Preprocessing

Conversion of pickup_datetime to datetime format.
Extraction of features: year, month, day, hour, and weekday.
Removal of rows with zero or missing longitude/latitude values.

4. Feature Engineering

Validation of coordinate values.
Calculation of geodesic distance between pickup and dropoff points.
Removal of rows with invalid distances (NaN values).

5. Data Visualization

Fare Amount Distribution: Histogram to visualize fare distribution.
Correlation Matrix: Heatmap to show relationships between numerical features.

6. Data Cleaning

Dropped non-numeric and unnecessary columns.
Ensured consistency in numeric data types for model training.

7. Model Building and Evaluation

A) Random Forest Regressor

Splitting Data: 80-20 split for training and testing sets.
Model Training: RandomForestRegressor with 100 estimators.

Evaluation Metrics:
R2 Score
Mean Absolute Error (MAE)
Mean Squared Error (MSE)
Root Mean Squared Error (RMSE)

B) Multilinear Regression

Trained using LinearRegression().
Evaluated on the same metrics as Random Forest.

C) Decision Tree Regressor

Trained using DecisionTreeRegressor().
Evaluated similarly for comparison.

8. Model Performance Comparison:
   
   Random Forest emerged as the best-performing model with the highest R2 score and minimum error rates.

9. Feature Importance Analysis

Visualization of feature importances using a bar plot.
Key influencing features: distance, pickup_hour, pickup_day, and passenger_count.

10. User-Defined Prediction Function

Function: predict_fare()

Takes user inputs for pickup/dropoff coordinates, passenger count, and time-related details.
Predicts fare using the trained Random Forest model.
Ensures consistency in feature ordering with the training dataset.

11. Sample Output
    Predicted Fare: $15.75



