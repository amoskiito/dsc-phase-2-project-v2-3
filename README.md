# Phase 2 Project Description

![](How%20Darwin%20Horan%20Boosting%20His%20Real%20Estate%20Business%20With%20Facebook.jpg)

The housing market is booming and the demand to create more housing is higher than ever. I have been tasked by Alliance Realtors, a new housing developer in King County to assess the local housing market and identify the features that most influence home sale price especially when a home owner wants to buy a house to renovate or renovate their own for sell.

Stakeholder: Alliance Realtors

Business Problem: Alliance developers would like to help homeowners do home renovations that will contribute to a higher sale price of the home.

Business Question: What features should you consider when renovating a home that would ultimately lead to a higher sale price?

Performing multiple linear regression on past home sales can show how strong of a relationship there is between the sale price of a home and a particular feature. Knowing to what extent these features influence sale price can provide insight and confidence that your new renovation will not only be a desirable build but one that will sell at a price you feel comfortable with.

# Data Understanding
The project utilizes data from the King County House Sales dataset. This dataset was provided to us at the onset of analysis and contains home sale information from 2014 to 2015 in King County, WA. This dataset contains 21,597 homes and 21 features, including:

* `id` - Unique identifier for a house

* `date` - Date house was sold

* `price` - Sale price (prediction target)

* `bedrooms` - Number of bedrooms

* `bathrooms` - Number of bathrooms

* `sqft_living` - Square footage of living space in the home

* `sqft_lot` - Square footage of the lot

* `floors` - Number of floors (levels) in house

* `waterfront` - Whether the house is on a waterfront
Includes Duwamish, Elliott Bay, Puget Sound, Lake Union, Ship Canal, Lake Washington, Lake Sammamish, other lake, and river/slough waterfronts

* `view` - Quality of view from house
Includes views of Mt. Rainier, Olympics, Cascades, Territorial, Seattle Skyline, Puget Sound, Lake Washington, Lake Sammamish, small lake / river / creek, and other

* `condition` - How good the overall condition of the house is. Related to maintenance of house.

* `grade` - Overall grade of the house. Related to the construction and design of the house.

* `sqft_above` - Square footage of house apart from basement

* `sqft_basement` - Square footage of the basement

* `yr_built` - Year when house was built

* `yr_renovated` - Year when house was renovated

* `zipcode` - ZIP Code used by the United States Postal Service

* `lat` - Latitude coordinate

* `long` - Longitude coordinate

* `sqft_living15` - The square footage of interior housing living space for the nearest 15 neighbors

* `sqft_lot15` - The square footage of the land lots of the nearest 15 neighbors

# Data Cleaning and Exploration
We focused on features that can be included in a new construction, and those that can be applied to previously existing homes (ie. `condition`, `yr_built`, `yr_renovated`). Limitations of the data include possible multicollinearity among some variables, some variables having statistically significant issues with p-value greater than our alpha of .05, dealing with an outdated and a narrow timeframe data set, and possible outliers.We used visualizations to explore relationships within the dataset, eventually deciding to use the following features for use in our models:

* `bedrooms`
* `bathrooms`
* `sqft_living`
* `sqft_living15`
* `floors`
* `waterfront`
* `view`
* `grade`
* `sqft_basement`
* `zipcode`

Using an iterative approach to our model building we created multiple linear regression models. We revisited the data on several occasions, creating dummy variables and dropping features in an attempt to improve model performance.

## Results
![](Screenshot%202022-09-29%20163659.png)

Grade has a very strong influence on home sale price, each additional increase in grade sees an increase in mean sale price.

![](Screenshot%202022-09-30%20175656.png)

Condition has a very strong influence on home sale price, for a better condition we see an increase in mean sale price.

## Regression Modelling
In our final regression model using all of our selected features, we saw an increase in model performance based on our R-squared value from 31 percent (baseline) to 57.5 percent (final). Our final model also had a Root Mean Squared Error of 160949.34. On average, our model is off from the actual price by 160949.34 dollars. All model features had a p-value < 0.05 (our alpha/significance level), which tells us that all features have a statistically significant linear relationship with price except for bathrooms and grade dummies. While we did not pass our homoscedasticity assumption in our final model we did pass our independence, linearity, and normaility assumptions, which is good. Here are some observations from our chosen model:

With each additional floor added you can increase the home sale price by 24,290 dollars.

Homes on a waterfront see an increase in property value of 13,260 dollars.

Homes that are considered to have a 'Good' view(view_4) sell for 32,000 dollars more than those with no view.

Homes that are considered to have an 'excellent' view(view_5) sell for 84,420 dollars more than those with no view.

grade,sqft_above and sqft_living had the strongest positive correlations with home sale price.

## Recommendations
A homeowner who is renovating a house in King County, with features in this data set, can only really control 3 things:

1) year renovated, which affects:

2) grade,

3) condition and

4) sell_year

After renovations, a homeowner can expect a $59 increase, per year after the year it was last worked on. Find a house to renovate that has at least what is considered a 'Good' view. Homes built on these lots will see an increase in sale price of around 32,000 dollars.

Homes with grade_7(average) see a bigger increase in value than most other features. Renovating a house with grade_7(average) materials and design sees an increase in sale price of around 94,750 dollars.

Also to take into consideration is the condition of the house as houses with a good condition see an increase in sale price of around 52,000 dollars.

## Conclusion
Our model accurately fits only 57.5 percent of the data. While this is sufficient enough to make observations and insights, conclusions should be approached with caution. Additionally, a test for homoscedasticity failed in our final model, which is one of the assumptions for linear regression. Further exploration into the normalization and scaling of features might help pass that assumption. Future analysis and modeling might want to consider a couple of items:

Find more recent home sales data to get a more accurate picture of today's market. Finding home sale information before 2014 would also help to create a more in-depth analysis.
Include additional features in future models. Particularly zipcode, sqft_living, and condition.

For more information:

Please check out my jupyter notebook on: https://github.com/amoskiito/dsc-phase-2-project-v2-3/blob/main/student.ipynb

and presentation:

https://github.com/amoskiito/dsc-phase-2-project-v2-3/blob/main/KingCounty%20Presentation.pdf



