# demand_forecasting
NYC Citibike Demand Forecasting for 2022 & 2023

Shift the Bricks X-Challenge, Javad Mollakazemi, March 2022

## Overview
This is an accelerator for demand forecasting. In this accelerator, Citibike demand in NYC for one year from time of doing the project (rest of 2022 and part of 2023) will be forecasted.

## Solution
In the solution provided all the available Citibike demand historical data from Oct 2013 to Feb 2022 was used. A couple of naïve models were initially implemented to give a baseline forecasting error for comparison. Then a basic ARIMA model was used which was not very successful compared to the baseline forecasting. The autocorrelation of the data revealed the seasonality structure of the data that the Citibike data has three different seasonality daily, weekly, and yearly. This information was greatly helpful to improve the ARIMA model performance. Another useful technique I used was predicting differential of data instead of the original data and then transform the predicted differential back to the original data. The reason for this was that the differential of data is much more stationary than the original data and make the forecasting more accurate. As the final step, a grid search was done to add the final improvements to the model. Finally, the best model was used to do the one-year ahead forecast. 



Since the Citibike data is publicly available there are some resources which were helpful. I list thme here:

#### Data Sources:


1. * [Citibike NYC Trip History Data](https://s3.amazonaws.com/tripdata/index.html)
2. * [NYC Taxi Data](https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page)
3. * [Visual Crossing Hourly Weather Data for ZipCode 10001](https://www.visualcrossing.com/weather/weather-data-services)
4. * [2010 Neighborhood Tabulation Areas (NTAs)](https://www1.nyc.gov/site/planning/data-maps/open-data/census-download-metadata.page)


#### References:

        
1. A research article titled "A longitudinal study of bike infrastructure impact on bikesharing system performance in New York City” by Susan Jia Xu, and Joseph Y. J. Chow, at New York University (https://par.nsf.gov/servlets/purl/10113034)

2. Kaggle Competition on predicting bike rides in Capital Bikeshare program in Washington, D.C.
(https://www.kaggle.com/competitions/bike-sharing-demand/overview)

3. Blog post titled “Exploring Citibike Ridership Data” (https://medium.com/@jeffmarvel/exploring-citibike-ridership-data-94ddaf6aee40)

