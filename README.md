# python-api-challenge
Module 6 Challenge

# Weather and Vacation Analysis with WeatherPy and VacationPy

## Overview

This project analyzes weather data across over 500 cities worldwide to explore how weather varies with latitude. Use Python libraries such as `citipy`, `OpenWeatherMap API`, and visualization techniques to identify patterns in weather across different latitudes. Additionally, use this data to plan ideal vacation spots based on preferred weather conditions and locate nearby hotels using the `Geoapify API`.

## Parts

1. **WeatherPy**: Visualize and analyze weather data of cities.
2. **VacationPy**: Use weather data to identify ideal vacation locations and nearby hotels.

### Part 1: WeatherPy

#### Description

In WeatherPy, a Python script is used to visualize the weather of over 500 cities. The script explores how weather parameters like temperature, humidity, cloudiness, and wind speed vary with latitude.

#### Linear Regression Analysis Summary

##### Temperature vs. Latitude
- **Northern Hemisphere**: Strong negative correlation between temperature and latitude, indicating temperatures decrease as you move away from the equator. Statistically significant with a very strong r-value.
- **Southern Hemisphere**: Strong positive correlation, showing temperatures increase closer to the equator. High statistical significance reflects consistent geographical trends.

##### Humidity vs. Latitude
- **Northern Hemisphere**: Mild positive correlation suggesting a slight increase in humidity with increasing latitude. The relationship, while statistically significant, is relatively weak.
- **Southern Hemisphere**: Similar weak positive correlation as the Northern Hemisphere but less pronounced, with lower statistical significance.

##### Cloudiness vs. Latitude
- **Northern Hemisphere**: Very weak positive correlation with marginal significance, indicating almost negligible relationship between cloudiness and latitude.
- **Southern Hemisphere**: Also a weak correlation, slightly stronger than in the Northern Hemisphere but lacking significant statistical backing.

##### Wind Speed vs. Latitude
- **Northern Hemisphere**: Very weak positive correlation showing minimal changes in wind speed with latitude, not statistically significant.
- **Southern Hemisphere**: Weak negative correlation, suggesting a slight decrease in wind speed as latitude increases, but this relationship lacks strong statistical support.

### Part 2: VacationPy

#### Description

Using the weather data from WeatherPy, identify potential vacation spots that meet specific weather criteria. Display these locations on a map and find hotels within 10,000 meters using `Geoapify API`.

#### Steps

- Filter `city_data_df` to meet ideal weather conditions.
    - Temperature between 65°F and 75°F
    - Wind speed less than 4.5 m/s
    - Zero cloudiness
- Display cities on a map with points scaled to humidity levels.
- For each city, find the first hotel within 10,000 meters.
- Include hotel name and country in the hover tooltip on the map.

## Admin Note

> **Important:** The `VacationPy` Jupyter notebook includes a map plot using `hvplot.points()`, which does not render directly on GitHub due to limitations of GitHub's static rendering of Jupyter notebooks. Therefore, I decided to include screenshots of my map plots and included them as `.png` files in the repository.
>
> This workaround addresses a GitHub limitation and is not due to an error on my part. Saved map plots as `.png` files were not originally required in the homework instructions.
