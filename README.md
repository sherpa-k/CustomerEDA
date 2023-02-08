# Exploratory Data Analysis on Airbnb Data

## Introduction
Airbnb, short for "Air Bed and Breakfast", is an online marketplace allowing homeowners and property-owners to rent out their properties for homestays. Airbnb is in direct competiton with hotels and other home rental marketplaces. Currently Airbnb is in 191 countries with over 150 million hosts and has half a billion renters a year. In short, Airbnb is a successful company that thrives in tourist-driven cities near various attractions. 

## Data
The dataset we used was found here https://www.kaggle.com/datasets/arianazmoudeh/airbnbopendata, and uses data on Airbnb listings in NYC.

## Overview

### Data Understanding
The dataset used had a total of 102,599 rows/observations and 26 columns. In terms of missing data, we had 190,770 missing values/cells. In total, **7.15%** of our data set was missing. The data also included various columns including, neighbourhood (borough), neighbourhood group, price, room type, service fee, etc.

### Data Cleaning
Overall, the dataset was disorganized and fairly messy, therefore we carried out:

1) Changed all column names to consistent names (lowercase and seperated with an underscore between words).
2) Removed columns that had too many missing values (threshold we used was 50% missing data).
3) Fixed mispelt neighborhood group names (ex. brookln to Brooklyn).
4) removed observations with missing values for neighborhood groups.
5) removed observations with missing values for neighborhoods.
6) changed price to a numeric.
7) imputed missing prices with the average price for listings within the respective neighborhood group.
