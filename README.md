# Bike_Rental_Sharing_Analysis

bike_rental sharing systems are new generation of traditional bike rentals where whole process from membership, 
rental and return back has become automatic. Through these systems, user is able to easily rent a bike 
from a particular position and return back at another position. Currently, there are about over 500 
bike_rental-sharing programs around the world which is composed of over 500 thousands bicycles. Today, there 
exists great interest in these systems due to their important role in traffic, environmental and health issues. 

Apart from interesting real world applications of bike_rental sharing systems, the characteristics of data 
being generated by these systems make them attractive for the research. Opposed to other transport 
services such as bus or subway, the duration of travel, departure and arrival position is explicitly
recorded in these systems. This feature turns bike_rental sharing system into a virtual sensor network that 
can be used for sensing mobility in the city. Hence, it is expected that most of important events in 
the city could be detected via monitoring these data.

## Data Dictionary:

# Both hour.csv and day.csv have the following fields, except hr which is not available in day.csv

 - instant: record index
 - dteday : date
 - season : season (1:springer, 2:summer, 3:fall, 4:winter)
 - yr : year (0: 2011, 1:2012)
 - mnth : month ( 1 to 12)
 - hr : hour (0 to 23)
 - holiday : weather day is holiday or not (extracted from [Web Link])
 - weekday : day of the week
 - workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
 + weathersit : 
 - 1: Clear, Few clouds, Partly cloudy, Partly cloudy
 - 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
 - 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
 - 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
 - temp : Normalized temperature in Celsius. The values are derived via (t-t_min)/(t_max-t_min), t_min=-8, t_max=+39 (only in hourly scale)
 - atemp: Normalized feeling temperature in Celsius. The values are derived via (t-t_min)/(t_max-t_min), t_min=-16, t_max=+50 (only in hourly scale)
 - hum: Normalized humidity. The values are divided to 100 (max)
 - windspeed: Normalized wind speed. The values are divided to 67 (max)
 - casual: count of casual users
 - registered: count of registered users
 - cnt: count of total rental bike_rental including both casual and registered


#######################################################################################################
## Objectives
#######################################################################################################

 - Plot, examine, and prepare series for modeling
 - Extract the seasonality component from the time series
 - Test for stationarity and apply appropriate transformations
 - Choose the order of an ARIMA model
 - Forecast the series

########## Examine your data ########## 
    - Plot the data and examine its patterns and irregularities
    - Clean up any outliers or missing values if needed
    - tsoutliers() find the outliers
    - tsclean() is a convenient method for outlier removal and inputing missing values
    - Take a logarithm of a series to help stabilize a strong growth trend

########## Decompose your data ########## 
   
   # Does the series appear to have trends or seasonality?
    
   - Use decompose() or stl() to examine and possibly remove components of the series

########## Stationarity ########## 

   # Is the series stationary?
    
   - Use adf.test()
   - ACF, PACF plots to determine order of differencing needed

########## Autocorrelations and choosing model order ########## 
   
   - Choose order of the ARIMA by examining ACF and PACF plots
   -  Fit an ARIMA model with optimal parameters(p,d,q)

########## Evaluate and iterate ########## 

    
   - Check residuals, which should haven no patterns and be normally distributed
   - If there are visible patterns or bias, plot ACF/PACF. Are any additional order parameters needed?
   - Refit model if needed. Compare model errors and fit criteria such as AIC or BIC.
   - Calculate forecast using the chosen model





