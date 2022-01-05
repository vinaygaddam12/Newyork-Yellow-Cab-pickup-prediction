# Group AB
This is the Repository of Group AB for the group project(COMP6200) named "Yellow Taxi Demand Prediction in New York city"

## Project Overview:
In this Project we are dealing with the data of yellow taxi in the New York city where our major goal is to determine the number of pickups of yellow taxi cabs in the city
of New York with given location names and time.

## Installation
Python 3 (Anaconda Prompt)

## Dataset:
The dataset used for this project is from year 2016 January which is collected from TLC Trip Record Data https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page 

## Project description
Various steps were performed in this project which are explained below:  
**1. Data Cleaning**  
There are various steps performed while cleaning the data which is given below:  

* Pickup latitude and Pickup longitude  
In this step, the pickup co-ordinates which are outside the bounding box of New-York is plotted on the graph.  
  
* Drop-off latitude and Drop-off longitude
In this step, the drop-off co-ordinates which are outside the bounding box of New-York is plotted on the graph.   
 
* Trip Duration  
In this step, time stamps are converted to unix then percentile is calculated to find correct percentile value for removal of outliers.  

* Speed, Trip Distance and total fare  
In all the mentioned steps, after removal of outliers we are checking if there are more outliers for which percentile is calculated and based on the percentile value outliers are removed.  

* Remove outliers/erroneous points 
In this step, based on our above univariate analysis all outliers are removed.

**2. Data Preparation**
In data preparation, what we do is preparing data to be capable of modelling. Here it consist of two CLUSTERING and TIME-BINNING.We defined function to find the minimum distance between pick up locations and we clustered these points to different regions using Kmeans clustering.After clustering regions, We did time binning where we created 10 minute bins.Updated the dataset with two more columns 'pickup_cluster'(to which cluster it belogns to) and 'pickup_bins' (to which 10min interval the trip belongs to) and made them primary and secondary index.

**3. Smoothing**
As smoothing is necessary for the data to remove noisy data and get to know the pattrens . We used  pickupbins to get clusters for the time interval of 10 minutes to know how many pickups happened in that interval and also to know the missing values where there are no pickups. We retrived the data with zero pickups in certain time interval used. We then defined functions like fill_missing(For filling missing value data) and smoothing(smoothing the data).While filling the missing values it filled with zero's and after smoothing the data we filled it with average values which is the best method for smoothing the data.

**4. Modelling**
In this project we used basic time series prediction techniques like Moving averages, weighted moving averages and exponential moving averages to model the baseline models. Later we incorporated different time series features such as exponential average, holts-winter triple exponential average, fourier transforms to the model and performed regression models such as linear and random forest regressor models. We caluclated MAPE and MSE of each of them and compared with baseline model to find out best model to predict the taxi demand in newyork city.


## Group Members:
Vinay Kumar Reddy Gaddam (46180540)

Supriya Basnet (46116761)

Shamshuddin Dudekula (46176292)

Swathy Parippil Chandrasekharan (46131825)
