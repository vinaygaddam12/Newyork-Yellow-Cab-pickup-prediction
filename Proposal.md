
# Yellow Taxi Demand Prediction in New York city


## Project Summary
New York City is arguably the taxi capital of America and home of the classic yellow taxicab. In New York City, taxicabs come in two varieties: yellow and green; they are widely recognizable symbols of the city. Taxis painted yellow (medallion taxis) can pick up passengers anywhere in the five boroughs. Taxicabs are operated by private companies and licensed by the New York City Taxi and Limousine Commission (TLC). Over 200,000 TLC licensees complete approximately 1,000,000 trips each day. Here in this project, we are collecting data from official TLC website which contains the fields capturing pick-up and drop-off dates/times, pick-up and drop-off locations, trip distances, itemized fares, rate types, payment types, and driver-reported passenger count from which we will analyze the total number of pick-ups available in the particular regional zone. To complete this project, we made some goals that need to be achieved and a plan that defines a way to achieve those goals. Following this we gave a brief description of the dataset we are using following that we gave techniques we planned to use to complete the project and finally, an outline of data is given.
## Goals
The major goal of this project is to determine the number of pickups of yellow cabs in the city of New York with given location names and time. For achieving the solution for this project with less error we need to achieve some goals.
Our goals to be achieved are,

i.	Remove erroneous points from the dataset by using bivariate and univariate analysis techniques.

ii.	Make clusters using by locations using Geo Haversine Distance and K means.

iii.	Create Time bins such that each time bin has at least one pick up. 

iv.	Create a Baseline model using Moving Windows and Weighted moving windows techniques and compute required MAPE and MSE.

v.	Use different regression analysis techniques like Linear regression, Random Forests, and Support Vector Machines by adding features using Fourier transforms and Holt-Winters Forecasting and compute MSE and MAPE.
## Briefing Dataset 
We got this dataset from the New York cabs Taxi & limousine commission (URL: https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page). This is the Government maintained website that notes trip details of every month in each year.  For the analysis, we only use Yellow cabs datasets. These are the famous NYC yellow taxis that provide transportation exclusively through street-hails. This dataset has different columns include pickup and drop off locations, fare, trip distances, payment type, passenger_count, tip amount, toll amount, improvements surcharge, and total amount. For this data set, we intend to do data processing and perform time series forecasting and regression analysis to predict pickups at a certain time.


## Techniques used
Firstly, we intend to remove outliers based on latitude and longitude, based on government rules on taxis. We divide data into clusters using k-means. We create some time bins which helps up to combine all pickups. Following by, time series analysis and create models using the Linear regression model. Data visualization through graphs is also very important in analysis.
## Plan
The project plan for our project is given below:

### Preparing the data for analysis:

•	We will remove outliers that are present in our dataset which is based on latitude, longitude, and government rules on taxis.

•	To understand the data structure clustering of data should be done for which the K-means algorithm will be used because of its simplicity.

•	To prepare the data for further processing data smoothing technique such as binning will be used which will create time bins of peak up hours.

### Applying analysis 

•	Time series analysis will be used, and a model is created by using linear regression for prediction purposes, which helps us to predict accurate pickups in different clusters at a specific time.

## Data Exploration
This data contains Yellow Taxi pickups in New York City. And this dataset is majorly focussed on below information:

i.	This trip data contains pickup and drop-off time, with detailed location information and distance travelled.

ii.	tpep_pickup_datetime: The date and time when the trip started.

iii.	Tpep_dropoff_datetime: The date and time when the trip ended.

iv.	Trip Distance: Trip distance travelled in miles.

v.	Pickup_location: Location where the trip started.

vi.	Dropoff_location: Location where the trip ended.


