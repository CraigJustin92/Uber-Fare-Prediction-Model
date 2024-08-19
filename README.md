# Uber Fare Amount Prediction

This project develops a model to predict Uber fare amounts using features such as distance traveled, number of passengers, and time of day (rush hour).

source of dataset: https://www.kaggle.com/datasets/kushsheth/uber-ride-price-prediction/data

## Summary
The project involved:
- **Data Cleaning:** Validated coordinates and selected relevant features.
- **Feature Engineering:** Calculated distance between pickup and dropoff locations. Added a `season` feature based on pickup date.
- **Data Transformation:** Log-transformed `fare_amount` to address right skewness and normalize the distribution.
- **Scaling:** Applied `StandardScaler` to ensure features are on a similar scale for better model performance.

## Findings
- **Correlation:** Distance and fare amount have a strong correlation (Pearson coefficient of 0.74).
- **Model Performance:** 
  - **R-squared:** 0.634, indicating the model explains 63.4% of the fare amount variation.
  - **Adjusted R-squared:** Confirms effective model performance with selected features.
  - **Coefficients:** 
    - Distance: $0.37 increase per mile.
    - Passenger count: $0.005 increase per passenger.
    - Rush hour: $0.01 increase during rush hours.
  - **Mean Squared Error (MSE):** 0.080.
  - **Mean Absolute Error (MAE):** 0.207.

- **Residual Analysis:** The model’s residuals are approximately normally distributed with some deviations, indicating possible outliers or non-normality.
