
# Module 2 Final Project - Housing Price Predictor

For: Premiere Property Management, LLC

By: Jenny Wadkins

## Introduction

>Premiere Property Management has asked me to develop a housing predictor tool. The market recently has exploded with volatility and unpredictability, with houses going 30k, 50k or even 100k over asking. Realtors need a better tool to price and predict homes. The tool should be easy to both use and understand.

## Questions

* What are the primary factors influencing housing prices in the King County metro area?
* Can we effectively use a regression model based system for realtors to determine a proper list price?
* Is a model-based system more accurate for determining list price than the traditional comps-based system?
* What easy-to-use features can we add to our model to increase its accuracy?

## Methodology
* Source data from King County
* Clean and prepare data for model processing
* Process data with a variety of models to find the most effective model
* Provide a "realtor simulator" model to compare with machine learning model
* Demonstrate ability of model to make new predictions

## Table of Contents

#### [student.ipynb](https://github.com/threnjen/dsc-mod-2-project-v2-1-online-ds-sp-000/blob/master/student.ipynb

> Notebook Preparation
* Recommended Extensions
* Importing our Modules
* Notebook-wide Functions

> Preprocessing
* Initial EDA
* Preparing Target Variable
* Preparing Categorical Variables
* Preparing Continuous/Ordinal Variables

> Visualizations with Geopandas

> Model Exploration
* Basic Linear Regression Model
* Linear Regression with Feature Selection Methods
* LAD Linear Regression
* Regularization Models - Lasso, Ridge, Elastic Net
* K-Nearest Neighbors
* Support Vector Regression
* Gradient Boosting Regressor
* Random Forest Regressor
* Comps "Model" - Realtor Simulator

> Regression Results and Model Selection

> Final Model
* Standardization Function
* Saving Model for later
* Preparing matrix for new predictions

> Making New Predictions

> Explanation of Attempts - Feature Engineering/Selection

> Conclusions
* Answers to business questions

> Recommendations

> Future Work


#### [predictor.ipynb](https://github.com/threnjen/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/predictor.ipynb)
* Separate page to make new predictions with the final model


## Analysis and Conclusion

#### What are the primary factors influencing housing prices in the King County metro area?
> Stuff here
![Figure 1 - Net Income of Franchise vs Non-Franchise](https://github.com/threnjen/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/franchise_vs_non.png)

#### Can we effectively use a regression model based system for realtors to determine a proper list price?
> Stuff here
![Net by Rating](https://github.com/threnjen/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/net_by_rating.png)

#### Is a model-based system more accurate for determining list price than the traditional comps-based system?
> Stuff here
![Net by Genre](https://github.com/threnjen/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/net_by_genre.png)

#### What easy-to-use features can we add to our model to increase its accuracy?
> Stuff here



## Recommendations



## Future Work

King County in particular offers comprehensive map data which can be integrated into our work via geopandas. These maps include information on school district and average household income which I suspect would be strong predictors. Utilizing the King County plot lookup map, our realtors would be able to enter an address which would be converted to a lat/long, and then utilized via web scraper at GreatSchools.org to determine the property's exact school assignments. We can also use the King County map information to determine other metrics such as parks and public services, as King County offers data for all of this information.
We also might be able to scrap Redfin for a walkability metric, but it may be more valuable to develop our own.

## Presentation
[Video - Data Science Module 1 Project](https://youtu.be/gkHU8ZpayuI)

[PDF of Presentation](https://github.com/threnjen/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/presentation.pdf)
