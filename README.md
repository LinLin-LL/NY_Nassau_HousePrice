# New York Nassau County House Prices Prediciton: Project Overview 
* Created a demo that estimates house prices in Nassau County (RMSE ~ $ 196K, MAE ~ $ 101K)
* Residential property sales from Jan 2008 to May 2018
* Optimized XGBoost Regressors using GridsearchCV to reach the best model. 


## Code and Resources Used 
**Python Version:** 3.7  
**Packages:** pandas, numpy, sklearn, xgboost, matplotlib, seaborn  


## Data Cleaning
*	Updated school district numbers
* Combined similar amenities to single features
*	Removed columns with over 5000 missing values and irrelavent columns
* Removed duplicated rows 
*	Transformed built year into age of house
*	Extracted year, month, day from sales date 

## EDA
I looked at the distributions of the data and the value counts for the various categorical variables. Below are a few highlights from the pivot tables. 

![alt text](https://github.com/LinLin-LL/NY_Nassau_HousePrice/blob/master/city.png "Sales by City")
![alt text](https://github.com/LinLin-LL/NY_Nassau_HousePrice/blob/master/y.png "House prices")
![alt text](https://github.com/LinLin-LL/NY_Nassau_HousePrice/blob/master/cor.png "Correlations")

## Model Building 

First, I transformed the categorical variables into dummy variables. I also split the data into train and tests sets with a test size of 20%.   

I tried Xgboost model because it handles missing values. I chose RMSE to tune parameters because it also penalizes large errors more.

## Model performance on test set
*	**XGBoost** : RMSE = 196264.51, MAE = 100538.87
