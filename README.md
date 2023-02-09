# Exploratory Data Analysis on Airbnb Data

## Introduction
Airbnb, short for "Air Bed and Breakfast", is an online marketplace allowing homeowners and property-owners to rent out their properties for homestays. Airbnb is in direct competiton with hotels and other home rental marketplaces. Currently Airbnb is in 191 countries with over 150 million hosts and has half a billion renters a year. In short, Airbnb is a successful company that thrives in tourist-driven cities near various attractions. 


## Data
The dataset we used was found here https://www.kaggle.com/datasets/arianazmoudeh/airbnbopendata, and uses data on Airbnb listings in NYC.

## Overview

### Required Packages
knitr\
tidyverse\
tidytext\
geomtextpath\
wordcloud\
RColorBrewer\
tm

### Data Understanding
The dataset used had a total of 102,599 rows/observations and 26 columns. In terms of missing data, we had 190,770 missing values/cells. In total, **7.15%** of our data set was missing. 

Dictionary of columns in data:

| Column | Description |
| ----- | ----- |
| id | Unique identifier |
| name | Name/description used on Airbnb listing |
| host_id | Host's identifier |
| host_identified_verified | Confirms if the host is a verified host |
| host_name | Name of the host |
| neighbourhood_group | Borough |
| neighbourhood |Neighbourhood of the borough |
| lat | Latitude |
| long | Longitude |
| country | Country |
| country_code | Country_code| 
| instant_bookable | T/F if listing can be booked immediadely |
| cancellation_policy | Flexibility of cancellation |
| room_type | type of listing (home/room/hotel) |
| Construction year | Year it was built |
| Price | Rental price |
| service_fee | Airbnb profit |
| minimum_nights | Minimum amount of stay |
| number_of_reviews | Amount of reviews on Airbnb |
| last_review | Date of last review |
| reviews_per_month | Average number of reviews per month |
| review_rate_number | Total average of reviews |
| calculated_host_listings_count | Amount of guests.
| availability 365 | number of days the property is available in the year |
| house_rules | Rules for the guests |



### Data Cleaning
Overall, the dataset was disorganized and fairly messy, therefore we carried out:

1) Changed all column names to consistent names (lowercase and seperated with an underscore between words).
2) Removed columns that had too many missing values (threshold we used was 50% missing data).
3) Fixed mispelt neighborhood group names (ex. brookln to Brooklyn).
4) removed observations with missing values for neighborhood groups.
5) removed observations with missing values for neighborhoods.
6) changed price to a numeric.
7) imputed missing prices with the average price for listings within the respective neighborhood group.
8) For remaining missing numeric values, we removed them all.

Ultimately, we are now left with 84,727 observations and 20 variables.

### Data Analysis

Looking at the distribution of prices, we can see that the average cost of an Airbnb in NYC per night came out to be $626.16 across all 5 boroughs. 
To split it up by boroughs :
| Borough	| Listings | Average Price |
| --- | --- | --- |
| Brooklyn | 35154	| 627.54|
| Manhattan |	35128	| 623.18 |
| Queens |	11301	| 630.56 |
| Bronx	| 2310	| 630.22 |
| Staten Island	| 834 |	622.47 |

