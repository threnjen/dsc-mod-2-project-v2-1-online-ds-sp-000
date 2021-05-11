
# Module 2 Final Project - Housing Price Predictor

For: Premiere Property Management, LLC

By: Jenny Wadkins

## Introduction

>Premiere Property Management has asked me to develop a housing predictor tool. The market recently has exploded with volatility and unpredictability, with houses going 30k, 50k or even 100k over asking. Realtors need a better tool to price and predict homes. The tool should be easy to both use and understand, and use features that a realtor can input.

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

> Preprocessing
* Initial EDA
* Process Data for Modeling

> Model Explorations
* Basic Linear Regression Model
* Linear Regression with various Feature Selection Methods
* LAD Linear Regression
* Regularization Models - Lasso, Ridge, Elastic Net
* K-Nearest Neighbors
* Support Vector Regression
* Gradient Boosting Regressor
* Random Forest Regressor
* RFECV with Mean Encoded Categoricals

> Realtor Simulator - the Classic Comps Model
* Write realtor simualtor functions and apply to test data

> Regression Results and Model Selection
* Evaluate results of all attempted models and choose best model

> Final Model
* Process and train final model on data
* Saving model assets for later use

> Making Predictions with New Data
* Making new predictions on one entry or imported csv

> Visualizations
* Feature visualizations
* Geopandas geographical visualizations
* Comps model geographical visualization

> Conclusions and Recommendations
* Answers to business questions

> Future Work

> Explanation of Attempts - Feature Engineering/Selection


## Analysis and Conclusion


#### What are the primary factors influencing housing prices in the King County metro area?
> As they say, location is everything, and it is the primary influencing factor for a home price in the King County metro area. Square footage of the house and grade of materials also strongly influence a home's price. These three features alone explain 85% of the price variation.
![Figure 1 - Housing Sales in King County by Location](https://github.com/threnjen/dsc-mod-2-project-v2-1-online-ds-sp-000/blob/master/images/map_housing_dots_cropped.png)

![Figure 2 - Total Price per Total Square Footage, by Grade](https://github.com/threnjen/dsc-mod-2-project-v2-1-online-ds-sp-000/blob/master/images/pr_grade.png)

![Figure 3 - Price per Square Foot per Total Square Footage, by Zip Code Median](https://github.com/threnjen/dsc-mod-2-project-v2-1-online-ds-sp-000/blob/master/images/pr_sf_zip.png)

#### Can we effectively use a regression model based system for realtors to determine a proper list price?
> Our regression model, while explaining over 88% of the price variance with our features, was nonetheless far from accurate in absolute terms. A mean average error of 56k in either direction is a huge variance to a home price - one that is so large that it renders the prediction much less meaningful and useful. Other models need to be explored, or better yet, easy-to-use features that an average realtor is capable of evaluating/acquiring should be added to the model to improve its predictive quality.

#### Is a model-based system more accurate for determining list price than the traditional comps-based system?
>At present, the regression model is only slightly more accurate than the comps-based system on our test data - and this is even with our comps-based simulator lacking a feature set as robust as our model. In fact our realtor simulator performed better on new data than our model. The model is lacking predictive features, and we should identify and include them.
![Figure 1 - Housing Sales in King County by Location](https://github.com/threnjen/dsc-mod-2-project-v2-1-online-ds-sp-000/blob/master/images/comps_plat.png)

#### What easy-to-use features can we add to our model to increase its accuracy?
> If we add features to the model, they need to be ones that an average realtor is capable of finding and utilizing with average Google skills. We could also add GUI features and web scraping to the backend that allows some of these things to be run by the model software. For example, using latititude and longitude, GreatSchools.org can tell a property's exact school assignments and ratings. A realtor doesn't know lat and long, but we can use under the hood web scraping that takes the address and uses a reverse address finder such as at https://www.latlong.net/Show-Latitude-Longitude.html to determine lat/long, then takes that result to GreatSchools.org to scrape for school information. Lat/long can also be utilized within the model in combination with the many GIS map tools available from King County about public services, parks, school districts, area income and more to obtain and enter data without the realtor needing to do any more than enter an address.


## Recommendations for Future Work

For future work, I'd like to see us start with a better data set than what is available here. Public records should allow a more robust set of features which will have sale type and allow us to eliminate non-market sales.

King County in particular offers comprehensive map data which can be integrated into our work via geopandas. These maps include information on school district and average household income which I suspect would be strong predictors. We can also use the King County map information to determine other metrics such as parks and public services, as King County offers data for all of this information.

If we add features to the model, they need to be ones that an average realtor is capable of finding and utilizing with average Google skills. We could also add GUI features and web scraping to the backend that allows some of these things to be run by the model software. For example, using latititude and longitude, GreatSchools.org can tell a property's exact school assignments and ratings. A realtor doesn't know lat and long, but we can use under the hood web scraping that takes the address and uses a reverse address finder such as at https://www.latlong.net/Show-Latitude-Longitude.html to determine lat/long, then takes that result to GreatSchools.org to scrape for school information. Lat/long can also be utilized within the model in combination with the many GIS map tools available from King County about public services, parks, school districts, area income and more to obtain and enter data without the realtor needing to do any more than enter an address.

## Presentation
[Video - Data Science Module 1 Project](https://youtu.be/gkHU8ZpayuI)

[PDF of Presentation](https://github.com/threnjen/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/presentation.pdf)
