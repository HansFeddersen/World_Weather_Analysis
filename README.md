# World_Weather_Analysis

Data Bootcamp Module 6: WeatherPy with Python APIs
## Overview of Project

### The purpose of this project is to retrieve information by using APIs (application programming interface) to visualize weather data from coordinates and create a vacation itinerary according to some criteria. The used coordinates were random generated (random library), the weather information was retrieved from OpenWeatherMap (https://openweathermap.org/, and the mapping was done using Google Maps APIs.

## Resoruces
**For this analysis, the following resuorces were used**:
- Data Sources: Open Weather Map, Google Maps
- Software: Jupyter Notebook 4.8
- Libraries: pandas, NumPy, Request and gmaps.

## Process

**Step 1: Weather Data**

- To start the project, first we create 2,000 random latitudes and longitudes using the function random (inlcuded in NumPy) with the following code:

![This is an image](https://github.com/HansFeddersen/World_Weather_Analysis/blob/main/more/setp1/Random_coordinates_generator.png)

- Then we pair each latitude and longitude created (by index) to search the nearest city and storage that city in a new list by ussing the append function:

![This is an image](https://github.com/HansFeddersen/World_Weather_Analysis/blob/main/more/setp1/Nearest_city_coordinates.png)

- Then we retrieve the weather data for each of the cities: 

![This is an image](https://github.com/HansFeddersen/World_Weather_Analysis/blob/main/more/setp1/Retrieve_weather_data.png)

- Convert the data to a DataFrame:

![This is an image](https://github.com/HansFeddersen/World_Weather_Analysis/blob/main/more/setp1/Convert_to_DataFrame.png)

- Save and convert the DataFrame as a CSV:

![This is an image](https://github.com/HansFeddersen/World_Weather_Analysis/blob/main/more/setp1/Convert_to_CSV.png)

**Step 2: Vacation Search**

- After importing the dependencies and csv, we ask the user to input the temperature limits:

![This is an image](https://github.com/HansFeddersen/World_Weather_Analysis/blob/main/more/step2/Input_limits.png)

-We convert all of the cities that enter between the two temperatures to a new DataFrame using the Loc Method:

![This is an image](https://github.com/HansFeddersen/World_Weather_Analysis/blob/main/more/step2/Input_criteria_DF.png)

-After we drop all the empty lines, we use gmpas to get the closest hotel (acording to defined parameters) to each city and store it in a new DF:

![This is an image](https://github.com/HansFeddersen/World_Weather_Analysis/blob/main/more/step2/Hotel_DF.png)

- We plot all the hotels in a map, adding a info box:

![This is an image](https://github.com/HansFeddersen/World_Weather_Analysis/blob/main/more/step2/Hotels_plot.png)

- At the end, the maps looks like this:

![This is an image](https://github.com/HansFeddersen/World_Weather_Analysis/blob/main/Vacation_Search/WeatherPy_vacation_map.png)

**Step 3: Vacation Itinerary**

- After we import the dependencies and load the csv, we choose 4 cities in the same country to make the itinerary. In this case, the cities are Houston, San Angelo, Desert Hot Springs and Deer Park:

![This is an image](https://github.com/HansFeddersen/World_Weather_Analysis/blob/main/more/step3/4_cities.png)

- We get the latitude and longitude for each of th 4 cities and create a layer map that shows the route between the 4 cities (in this case is the driving route):

![This is an image](https://github.com/HansFeddersen/World_Weather_Analysis/blob/main/more/step3/driving_route.png)

The final map is as follows:

![This is an image](https://github.com/HansFeddersen/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map.png)

- To draw a new map that only contains the 4 cities, we use the concat function to combine the cities into one DataFrame, then we create the info box to our map and output the new map:

![This is an image](https://github.com/HansFeddersen/World_Weather_Analysis/blob/main/more/step3/New_map.png)

- Finally, the new map is as follows:

![This is an image](https://github.com/HansFeddersen/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map_markers.png)
![This is an image](https://github.com/HansFeddersen/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map_markers_2.png)

