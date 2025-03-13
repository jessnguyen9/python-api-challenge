# WeatherPy: Exploring Weather Trends

## Overview
This project analyzes weather patterns across various global cities using data from the OpenWeatherMap API. It demonstrates how weather variables such as temperature, humidity, cloudiness, and wind speed correlate with latitude. The insights are useful for businesses, travelers, and climate researchers.

## Data Source
- **Geographic coordinates:** Randomly generated using NumPy

- **City names:** Identified using the Citipy library

- **Weather data:** Fetched from the OpenWeatherMap API

## Tools & Techniques Used
### Data Acquisition
Used NumPy to generate random latitude and longitude values

Identified the nearest cities using Citipy

Fetched real-time weather data from OpenWeatherMap API

### Data Preparation
Cleaned the data by handling missing values and API request failures

Extracted relevant weather attributes: temperature, humidity, cloudiness, wind speed, country, and date

Converted timestamp data into human-readable format

Stored the final dataset in a structured Pandas DataFrame

### Data Analysis & Visualization
Explored relationships between latitude and key weather attributes

Created scatter plots to visualize trends:

- **Latitude vs. Temperature:** Examined how temperature varies with latitude

![City Max Latitude vs  Temperature (2022-10-18)](https://github.com/user-attachments/assets/4f984623-9705-4df5-ab19-236709d0310e)

- **Latitude vs. Humidity:** Assessed humidity distribution across latitudes

- **Latitude vs. Cloudiness:** Identified cloud cover patterns

- **Latitude vs. Wind Speed:** Analyzed how wind speed changes with latitude

Used Matplotlib for clear, insightful visualizations
