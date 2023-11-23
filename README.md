Module-6-API-Challenge

Part 1: Weather
In this part of the assignment, a Python script is used to visualize the weather of over 500 cities of varying distances from the equator. 

Files:
    WeatherPy.ipynb
        This is a Jupyter Notebook file which contains Python code to do the following;
            - randomly generate up to 1500 sets of latitude and longitude co-ordinates
            - use the CityPy package to find a city close to each of these co-ordinates. Some sets of co-ordinates will be unsuccessful. The cities found are saved to a csv file in the          output_data folder
            - an external site ,the OpenWeatherMap, is used via API requests to get the weather for each of the cities found
            - graphs are then plotted to show the relationships between latitude and a set of weather conditions (max. temperature, humidity, cloudiness and wind speed) on that day. The subsequent graphs are saved to the output_data folder
            - regression graphs are plotted to show the differences bewteen the northern and southern hemispheres for each of the weather conditions

    output_data/cities.csv  A list of cities with data on their latitudes, longitudes, max. temp, humidity, cloudiness, wind speed and date that the weather was accessed
    output_data/Fig1.png:   A graph of lattitude vs max. temperature
    output_data/Fig2.png:   A graph of lattitude vs humidity
    output_data/Fig3.png:   A graph of lattitude vs cloudiness
    output_data/Fig4.png:   A graph of lattitude vs wind speed

Part 2: Vacation
In this part of the assignment the weather data accessed for Part 1 is used to plan future vacations. 

Files:
    VacationPy.ipynb
         This is a Jupyter Notebook file which contains Python code to do the following;
            - plot the cities found in Part 1 and stored in output_data/cities.csv on a map using the hvplot package
            - use the cities stored in output_data/cities.csv to find the cities with an ideal set of weather conditions using the following criteria,
                o	A max temperature lower than 27 degrees but higher than 21
                o	Wind speed less than 4.5 m/s
                o	Zero cloudiness
            - the nearest hotel is then found in each of these cities with the ideal conditions using API requests to the website Geoapify.com
            - the ideal vacation cities are then plotted on a map along with hotel name and country using hvplot
