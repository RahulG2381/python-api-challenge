# Python-API-Challenge
## Challenge Description
This challenge has been split into two deliverables. The first 'WeatherPy' tasked to obtain the weather from the 'OpenWeatherMap API' for 500 cities across the world, with the data collected and being output to a CSV file before being read into the second task 'VacationPy'. In the second task, using the data within the CSV, locate hotels using the 'Geoapify API' within certain Cities.
## WeatherPy
To work on this challenge WeatherPy.ipynb and VacationPy.ipynb starter code files were already been provided. I have built my code to generate random geographic coordinates and the nearest city to each latitude and longitude which is used in later to find the relationship of each city coordinates and the variable by plotting them into scatter plots.
•	Latitude vs. Temperature
•	Latitude vs. Humidity
•	Latitude vs. Cloudiness
•	Latitude vs. Wind Speed
Then I have append all the data to “city_data” list and created a data frame to save all the cities  records into csv data file named “cities” and capture all four relationship figures (Fig1, Fig2, Fig3 and Fig4)  into “ output_data”. 
Then in later stage I have computed the linear regression for each relationship. Separate the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude). 
Next, I have created a series of scatter plot with the linear regression line, the model's formula, and the r values which help to evaluate the graphs and analyse the data. 
•	Northern Hemisphere: Temperature (C) vs. Latitude
•	Southern Hemisphere: Temperature (C) vs. Latitude
•	Northern Hemisphere: Humidity (%) vs. Latitude
•	Southern Hemisphere: Humidity (%) vs. Latitude
•	Northern Hemisphere: Cloudiness (%) vs. Latitude
•	Southern Hemisphere: Cloudiness (%) vs. Latitude
•	Northern Hemisphere: Wind Speed (m/s) vs. Latitude
•	Southern Hemisphere: Wind Speed (m/s) vs. Latitude
## VacationPy
Using the csv file I have created in previous sub challenge WeatherPy (city_data_df), plot the cities on a hvplot map. The size of the point was based on humidity in each city.

To limit the number of Cities I have applied following conditions 
1.	A max temperature lower than 27 degrees but higher than 21
2.	Wind speed less than 4.5 m/s
3.	Zero cloudiness

Then I have renamed the dataset to “hotel_df” and added one more column, named “ Hotel Name” so our new table is with following columns.
  City
•	Country
•	Longitude
•	Latitude
•	Humidity
•	Hotel Name

Locate nearest Hotel to each City in 'hotel_df'
The task was by using the 'Geoapify API' iterate through each City within the 'hotel_df' dataset and find the nearest Hotel with in 10000 meters of the Latitude and Longitude of the city and then, 
1.	Append the name of the hotel to the 'Hotel Name' column of the DataFrame
2.	Add the 'Hotel Name' and 'Country' to the hover message for each point!
