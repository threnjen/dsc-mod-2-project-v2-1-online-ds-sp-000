
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

> Regression Results and Model Selection

> Final Model
* Standardization Function
* Saving Model for later
* Preparing matrix for new predictions

> Comps "Model" - Realtor Simulator

> Making New Predictions

> Explanation of Attempts - Feature Engineering/Selection

> Conclusions
* Answers to business questions

> Recommendations

> Future Work



#### [predictor.ipynb](https://github.com/threnjen/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/predictor.ipynb)
* Separate page to make new predictions with the final model



## Analysis and Conclusion

#### Should Microsoft focus on launching a franchise, or focus on single film IPs?
> Franchises generally have a higher budget, but their failure rate is far less and they are more likely to a) be profitable and b) yield a surprise hit. They do, however, have a higher variance in both budget and net income. This risk is offset by the observation that franchise films rarely fail, whereas non-franchise films make up the majority of failed films in the last 20 years. A franchise is recommended.
![Figure 1 - Net Income of Franchise vs Non-Franchise](https://github.com/threnjen/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/franchise_vs_non.png)

#### What audience should the company aim for (based on MPAA rating)?
> Various analysis shows that a movie's performance range declines in both consistency and average net income as the rating increases from G to R. G movies have both the highest consistent income range, and the lowest rate of overall failure. PG is shortly behind. PG-13 is most likely to result in a breakout hit, but has a much lower consistent income range. Lower ratings are the safest and most consistent.
![Net by Rating](https://github.com/threnjen/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/net_by_rating.png)

#### What genre(s) should the company aim for?
> The genres of Adventure, Animation, Fantasy, Sci-Fi and Action are the most strongly correlated with a positive net income.
![Net by Genre](https://github.com/threnjen/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/net_by_genre.png)

#### What combination of genre, franchise and rating will result in the lowest risk?
> While franchises involve a higher variance in both budget and net, this risk is offset by their overall higher success rate, with very few franchise films failing to yield a positive net income. This risk is further reduced by sticking to lower MPAA ratings in the G or PG range, and selecting genres that complement these ratings from the animation, sci-fi, fantasy, adventure and action categories. Overall, a G or PG franchise that utilizes Animation and a complementary category such as Adventure should be a very safe endeavor.

#### What, if any, genres/ratings/franchises should be avoided?
> Analysis of the past 20 years first shows that non-franchise films both make less money and are more likely to fail. Most of the film failures in this time period were not franchises. Films are also more likely to fail as their MPAA rating increases. R-movies in particular have a very high rate of failure, with over 30% of the failures of the last 20 years rated R. Finally, certain genres are clearly more likely to fail, with the Drama and Comedy genres representing about 58% and 42% of failures respectively (these numbers add up to 100, but these genres may be shared together on one film, meaning that film is present in both numbers). Things to be avoided include non-franchise films, higher MPAA ratings, and the Comedy, Drama and Thriller categories. These things should certainly be avoided individually, and definitely avoided in combination.
![Failures by Rating](https://github.com/threnjen/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/bombs_by_rating.png)
![Failures of Non-Franchise vs Franchise](https://github.com/threnjen/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/franchise_status_fails.png)
![Failures by Genre](https://github.com/threnjen/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/failures_by_genre.png)

## Recommendations



## Future Work

King County in particular offers comprehensive map data which can be integrated into our work via geopandas. These maps include information on school district and average household income which I suspect would be strong predictors. Utilizing the King County plot lookup map, our realtors would be able to enter an address which would be converted to a lat/long, and then utilized via web scraper at GreatSchools.org to determine the property's exact school assignments. We can also use the King County map information to determine other metrics such as parks and public services, as King County offers data for all of this information.
We also might be able to scrap Redfin for a walkability metric, but it may be more valuable to develop our own.

## Presentation
[Video - Data Science Module 1 Project](https://youtu.be/gkHU8ZpayuI)

[PDF of Presentation](https://github.com/threnjen/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/presentation.pdf)
