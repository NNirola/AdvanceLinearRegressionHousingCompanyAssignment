# Surprise Housing Company
> Building a model for houses with the available independent variables. This model will then be used by the management to understand how exactly the prices vary with the variables. They can accordingly manipulate the strategy of the firm and concentrate on areas that will yield high returns. Further, the model will be a good way for management to understand the pricing dynamics of a new market.
Objectives:
- Variables are significant in predicting the price of a house
- Variables describe the price of a house
- Optimal values of lambda for ridge and lasso regression.

## Table of Contents
* [General Information](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)
* [Contact](#contact)

## General Information
- **Background:** A US-based housing company named Surprise Housing has decided to enter the Australian market. The company uses data analytics to purchase houses at a price below their actual values and flip them on at a higher price. For the same purpose, the company has collected a data set from the sale of houses in Australia. The data is provided in the CSV file below.
The company is looking at prospective properties to buy to enter the market. You are required to build a regression model using regularisation in order to predict the actual value of the prospective properties and decide whether to invest in them or not.
- **Business Problem:** The primary goal is to build a model for houses with the available independent variables. This model will then be used by the management to understand how exactly the prices vary with the variables. They can accordingly manipulate the strategy of the firm and concentrate on areas that will yield high returns. Further, the model will be a good way for management to understand the pricing dynamics of a new market.
- **Dataset:** The project uses the `train.csv` dataset, which contian list of data for US based company data set.
## Conclusions
#### Optimal Lambda (alpha) from GridSearchCV

| Model | Optimal alpha (λ) |
|---|---:|
| Ridge | 2.0 |
| Lasso | 0.001 |

#### Performance comparison (Ridge vs Lasso)

| Model | Split | MSE | R^2 | RSS | RMSE |
|---|---|---:|---:|---:|---:|
| Lasso | Train | 0.007438430039377301 | 0.928937802340879 | 3.6448307192948777 | 0.08624633348367512 |
| Lasso | Test | 0.01701443833402708 | 0.8777015866323229 | 2.0927759150853307 | 0.13043940483621919 |
| Ridge | Train | 0.005257330566085671 | 0.949774688762443 | 2.576091977381979 | 0.07250745179694064 |
| Ridge | Test | 0.018288216266787883 | 0.8685457733694272 | 2.2494506008149098 | 0.13523393163991013 |

#### Top-15 positive features (Ridge and Lasso)

##### Ridge Top 15 positive features
| Rank | Feature | Coefficient |
|---:|---|---:|
| 1 | GrLivArea | 0.206061 |
| 2 | TotalBsmtSF | 0.163914 |
| 3 | 1stFlrSF | 0.155363 |
| 4 | 2ndFlrSF | 0.144857 |
| 5 | BsmtFinSF1 | 0.143310 |
| 6 | Neighborhood_Crawfor | 0.114370 |
| 7 | GarageArea | 0.111369 |
| 8 | GarageCars | 0.107303 |
| 9 | YearBuilt | 0.098310 |
| 10 | OverallQual_9 | 0.097415 |
| 11 | SaleType_CWD | 0.092252 |
| 12 | Exterior1st_BrkFace | 0.089160 |
| 13 | FullBath | 0.087407 |
| 14 | OverallCond_8 | 0.078098 |
| 15 | OverallCond_9 | 0.077135 |

##### Lasso Top 15 positive features
| Rank | Feature | Coefficient |
|---:|---|---:|
| 1 | GrLivArea | 0.672571 |
| 2 | TotalBsmtSF | 0.194213 |
| 3 | YearBuilt | 0.154716 |
| 4 | GarageCars | 0.127411 |
| 5 | Neighborhood_Crawfor | 0.120677 |
| 6 | BsmtFinSF1 | 0.109661 |
| 7 | Functional_Typ | 0.086531 |
| 8 | OverallQual_8 | 0.073924 |
| 9 | OverallQual_9 | 0.071098 |
| 10 | Neighborhood_Somerst | 0.062442 |
| 11 | GarageArea | 0.059629 |
| 12 | BsmtCond_TA | 0.041404 |
| 13 | Condition1_Norm | 0.038232 |
| 14 | GarageYrBlt | 0.035759 |
| 15 | LandSlope_Mod | 0.035291 |

#### Recommended features for Sunrise Housing Company (prioritized by average positive impact across Ridge and Lasso)

| Rank | Feature | Ridge Coefficient | Lasso Coefficient | Priority (avg) |
|---:|---|---:|---:|---:|
| 1 | GrLivArea | 0.206061 | 0.672571 | 0.439316 |
| 2 | TotalBsmtSF | 0.163914 | 0.194213 | 0.179064 |
| 3 | YearBuilt | 0.098310 | 0.154716 | 0.126513 |
| 4 | BsmtFinSF1 | 0.143310 | 0.109661 | 0.126486 |
| 5 | Neighborhood_Crawfor | 0.114370 | 0.120677 | 0.117524 |
| 6 | GarageCars | 0.107303 | 0.127411 | 0.117357 |
| 7 | GarageArea | 0.111369 | 0.059629 | 0.085499 |
| 8 | OverallQual_9 | 0.097415 | 0.071098 | 0.084257 |
## Technologies Used
- pandas
- numpy
- scikit-learn
- statsmodels
- matplotlib
- seaborn
- sklearn

## Acknowledgements
- This project was completed as part of the IITB ML/AI Cohort assignment.

## Contact
Created by [@nnirola] - feel free to contact me!