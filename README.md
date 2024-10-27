# python-api-challenge

This assignment is divided into two parts.

## Part 1: WeatherPy
- The script in this seciton randomly selects 500+ sets of coordinates and the nearest city for each coordinate. These coordinates and cities are added to lists.
- Through the use of OpenWeather API, the script pulls weather data for all cities (max temp, relative humidity, wind speed, etc).
- This data is then added to the city_data_df DataFrame.
- city_data_df is exported to a csv file.
- Using city_data_df, the script created scatter plot charts comparing Latitude vs Max Temp, Latitude vs Humidity, Latitude vs Wind Speed.
- PNG files are created for each scatter plot.
- I added a function that calculates linear regression for latitude vs another variable. Two arguments need to be provided: dataframe name, y_value (e.g. max temp).
- The city_data_df DataFrame is split into two separate dataframes: one for cities in the Northern Hemisphere, the other for cities in the Southern Hemisphere.
- The linear regression function is used to plot charts for latitude vs max temp/humidity/wind speed for both DataFrames.

## Part 2: VacationPy
- The script imports the csv file created in Part 1 into a DataFrame.
- Using hvplot and the geoViews libraries, the script plots all of the cities on a map using the coorindates.
- Using specific criteria, I narrow down city_data_df to ideal_weather_df.
- I then copy city, country, coordinates, and humidity series into the newly created hotel_df.
- Using Geoapify API, the script goes through all of the cities and finds the first hotel within 10 km radius from the coordinates.
- A new map is created using hotel_df. The hover message shows country name and the selected hotel name.

Please note that API keys for Geoapify API and OpenWeatherMap API are required for this script.

# Included in this Repository:
  - README.md
  - WeatherPy directory
    - WeatherPy.ipynb
    - VacationPy.ipynb
    - output_data directory
      - Fig1.png
      - Fig2.png
      - Fig3.png
      - Fig4.png
      - cities.csv
