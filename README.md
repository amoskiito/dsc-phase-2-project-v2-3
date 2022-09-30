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
