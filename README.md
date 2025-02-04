# M2P07 - Regression Project

## Project Description 
This project analyzes information from containing rental prices for units in across Canada in 2024.

## Data Source
Dataset obtained from rentfaster.ca:
- https://www.rentfaster.ca/?utm_source=OOH&utm_medium=sign&utm_campaign=ca
The data dictionary can be found here:
- https://www.kaggle.com/datasets/sergiygavrylov/25000-canadian-rental-housing-market-june-2024

## Goal of the Analysis
Explore multiple regression models, in order to find a model that predicts the rental price most accurately.

## Analysis
### 1st Model applied - Linear Regression (Limited to a few columns, avoiding categorical columns)
- Price Mean is around 2156 CAD
- Error in the model around 617 CAD
- Error of 28% of the Mean value - significantly high the error.

### 2nd Model Applied - Linear Regression adding most categorical columns and Encoded Columns
- Price Mean is around 2156 CAD
- Error in the model around 500.41 CAD
- Error of 23% of the Mean value - Better than first model but yet high the error.

### 3rd Model Applied - Polynomial and then LASSO
- First step find the degree 1 was the best fit, because the 2nd is overfitting (means 1st degree is as the 2nd model)
- Then Applied LASSO - because LASSO helps to simplify the model and prevent overfitting.
- with LASSO found RMSE of 456,41 CAD less than the lineal regression in the 2nd model.

### Cross validation performed and at the end it was tested with the 2nd model.

## Result
###  2nd Model tested with Real Data from the Site rentfaster.ca
- Real data - https://www.rentfaster.ca/on/toronto/rentals/apartment/1-bedroom/pet-friendly/560595?-RSYNC
- Original Rental Price  - 2,025.00 CAD
- Predicted Rental Price - 1,916.84 CAD
- the predicted data is around 109 CAD below de real price, means an error of 5.35%

---
