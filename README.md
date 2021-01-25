# Project_2-Moneyball
# Predicting OBP of MLB players

## **Objective:**
Build a regression model to predict the OBP of MLB players.

## **Approach:**
Initially data from 26 features was gathered, but only 6 features were included in the final model (Age, Strikeouts, Homeruns, Stolent Bases, RBIs, Positions, Intentional Walks).  Additionally, feature engineering was done to add a multiplicative interaction term between the homeruns and RBIs.  The training data was evaluated on linear regression, ridge regression, and LASSO regression models, both with the features as is and standard scaled, in order to optimize for R2 and MSE.

## **Featured Techniques:**
- BeautifulSoup web scraping
- Feature Engineering & Selection
- Supervised Machine Learning
- Linear regression
- Regularization
- LASSO
- Ridge regression

## **Data:**
Data from more players over a 20-year period from 1999-2019 was gathered and cleaned as appropriate for the purposes of this project. Pitchers and players with less than 50 plate appearances in a season were not included. The data came from the website https://www.baseball-reference.com/leagues/MLB/2019-standard-batting.shtml.


## **Results Summary:**
A simple linear regression model with standard scaling of features was selected.  Features included in the final model are Age, Stolen Bases, Strikeouts, Homeruns, RBIs, Positions, Intentional Walks. The features were used to predict 5-year graduation rates. The model was optimized for R2 and mean square error using polynomial regression. On the test data, the model had a R2 of 0.74 and MSE of 112.4.
Data scraping and linear modeling for MLB OBP
