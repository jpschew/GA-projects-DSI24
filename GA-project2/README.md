# Project 2 - Ames Housing Data and Kaggle Challenge

### Using the Ames Housing Dataset that is available on [Kaggle](https://www.kaggle.com/c/dsi-us-6-project-2-regression-challenge), this project aims to identify features that are influential in predicting the housing price and determine the best regression model for predicting Sale Price of House in Ames. With this model, it will be beneficial to home owners and potential buyers for them to have an estimate gauge of the price in mind if they decided to sell or buy a property. It can be also useful to real-estate agents so they can help their customers to buy or sell a property at the appropriate price.

## Executive Summary

With more than 80 over features that could possibly influence the housing prices in Ames, it is impossible for buyers/sellers or even property agents to go through all the features one by one to decide on the sale price of a property. Hence, this project aims to create a regression model that can help to make prediction based on some of the more important features.

After coming out with 5 different models in this project, a Lasso regression model had a comparative performance with ElasticNet regression model in terms of root mean square error (RMSE). However, the Lasso regression model also results in more than 50% reduction in the features required in the other models, hence this model is chosen for the prediction of house price. The Lasso regression also show that the top 3 predictors are the location of the house (Neighborhood), the total living area above ground (Gr Liv Area) and the overall quality of the house (Overall Qual). With a given set of features, the model is able to predict the price of a house as the Lasso regression model produce the best fit coefficient for the respective features with a RSME score of 34264. 

One thing to take note of the Lasso regression model is that the actual test dataset has a better RMSE than the train dataset. This might due to overfitting, hence the model can still be improved by re-iterating and check which of the features can be filtered out to avoid overfitting.

However, in reality, alot of other factors not included in the present dataset can affect the sale price of a property. Hence, the aim of this model is to act as a guideline for sellers/buyers as well as property agents to have a estimate range of price given the features of a property.

Below show the table of comparison for the different models:

|  | Description | Hyperparameters | Number of Features | CV RMSE | Kaggle RMSE|
| :-: | :-: | :-: | :-: | :-: |:-:|
| Model 1 | Linear Regression | - | 2 | 49996.5 | 46816.55 |
| Model 2 | Linear Regression | - | 85 | 34992.97 | 35610.13 |
| Model 3 | Ridge Regression | alpha = 26 | 85 | 34541.8 | 34482.18 |
| Model 4 | Lasso Regression | alpha = 97.7 | 38 | 34328.89 | 34264.73 |
| Model 5 | ElasticNet Regression | alpha = 0.02, l1_ratio = 0.3 | 85 | 34546.9 | 34441.81 |

## Data Dictionary

| Feature | Feature Type | Data Type | Dataset | Description |
| --- | --- | --- | --- | --- |
| Total Bsmt BF | Continous | Float | Train/Test | Total Basement Area in Square Feet |
| Gr Liv Area | Continuous | Integer | Train/Test | Total Living Area above Ground in Square Feet |
| Overall Qual | Ordinal | Integer | Train/Test | Rating of Overall Material and Finish of the House |
| Exter Qual | Ordinal | Integer | Train/Test | Quality of Exterior Material |
| Heating QC | Ordinal | Integer | Train/Test | Quality and Condition of Heating |
| Kitchen Qual | Ordinal | Integer | Train/Test | Kitchen Quality |
| Garage Finish | Ordinal | Integer | Train/Test | Interior Finiah of Garage |
| MS SubClass | Nominal | Object | Train/Test | Type of Dwelling Sold|
| MS Zoning | Nominal | Object | Train/Test | General Zoning Classification |
| Lot Config | Nominal | Object | Train/Test | Lot Configuration |
| Neighborhood | Nominal | Object | Train/Test | Physical Locations within Ames City |
| House Style | Nominal | Object | Train/Test | Style of Dwelling |
| Roof Style | Nominal | Object | Train/Test | Roof Type |
| Exterior 1st | Nominal | Object | Train/Test | Exterior covering the the House |
| Exterior 2nd | Nominal | Object | Train/Test | Exterior covering the House if more than 1 Material |
| Mas Vnr Type | Nominal | Object | Train/Test | Masonary Veneer Type |
| Foundation | Nominal | Object | Train/Test | Foundation Type |
| Garage Type | Nominal | Object | Train/Test | Garage Location |
| SalePrice | Continuous | Integer | Train | Sale Price ($$) |