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

![City Max Latitude vs  Humidity (2022-10-18)](https://github.com/user-attachments/assets/c7ab30c9-d902-4fd6-bbb8-44477ea2ed7c)

- **Latitude vs. Cloudiness:** Identified cloud cover patterns

![City Latitude vs  Cloudiness (2022-10-18)](https://github.com/user-attachments/assets/404b6a30-90b4-487c-94ed-4d8cdc19e274)

- **Latitude vs. Wind Speed:** Analyzed how wind speed changes with latitude

![City Latitude vs  Wind Speed (2022-10-18)](https://github.com/user-attachments/assets/a7740722-afc7-4a6f-a594-cfbc90c0a569)

Used Matplotlib for clear, insightful visualizations

## Linear Regression Analysis
Linear regression was performed separately for cities in the Northern and Southern Hemispheres.

### Latitude vs. Temperature
**Northern Hemisphere Linear Regression**

![Temperature vs  Latitude Linear Regression Plot Northern](https://github.com/user-attachments/assets/2c2a4d81-f28e-4050-b168-9ab3be835dcf)

- R-value: -0.777672630162631

**Southern Hemisphere Linear Regression**

![Temperature vs  Latitude Linear Regression Plot Southern](https://github.com/user-attachments/assets/bce17606-9e90-4e0e-8fda-b504aeb588b8)

- R-value: 0.8321341504647478

**Key Insights: Latitude vs. Temperature**

- The closer a city is to the equator, the warmer it tends to be. On the other hand, temperatures drop as you move toward the North or South Pole. This pattern is clear in both hemispheres, but it’s slightly stronger in the Southern Hemisphere.

- One possible reason is that the Southern Hemisphere has more ocean, which helps keep temperatures more stable. In contrast, the Northern Hemisphere has more land, leading to bigger temperature changes.

- However, not all cities follow this pattern exactly. Some are warmer or colder than expected due to things like altitude, ocean currents, or local weather. This shows that while latitude is important, other factors also play a role in temperature.

### Humidity vs. Latitude
**Northern Hemisphere Linear Regression**

![Humidity vs  Latitude Linear Regression Plot Northern](https://github.com/user-attachments/assets/eac7ea18-48e0-4763-8d09-8f974a349071)

- R-value: 0.17699485278624

**Southern Hemisphere Linear Regression**

![Humidity vs  Latitude Linear Regression Plot Southern](https://github.com/user-attachments/assets/6f5a6ede-0ade-4abf-a106-ffe6466c937b)

- R-value: 0.09406704802059436

**Key Insights: Humidity vs. Latitude**

- Humidity doesn’t strongly depend on how far a place is from the equator. In the Northern Hemisphere, there’s a slight trend where humidity increases as you move north, while in the Southern Hemisphere, it decreases slightly. However, the relationship is weak, meaning latitude alone doesn’t determine humidity levels.

- Other factors like being near oceans, seasonal weather patterns, and local climate conditions play a much bigger role. For example, coastal cities often have high humidity regardless of latitude, while deserts, even near the equator, can be very dry.

### Cloudiness vs. Latitude 
**Northern Hemisphere Linear Regression**

![Cloudiness vs  Latitude Linear Regression Plot Northern](https://github.com/user-attachments/assets/edfbf54c-7c8d-4534-8ab0-2864674c1f5d)

- R-value: 0.08846982337474067

**Southern Hemisphere Linear Regression**

![Cloudiness vs  Latitude Linear Regression Plot Southern](https://github.com/user-attachments/assets/a225103f-5c9c-427c-922f-f4888331fa40)

- R-value: 0.052691182982807144

**Key Insights: Cloudiness vs. Latitude**

- There isn’t a clear connection between how cloudy a place is and how far it is from the equator. In the Northern Hemisphere, cloudiness slightly increases as you move north, while in the Southern Hemisphere, it slightly decreases. However, these trends are weak, meaning latitude alone isn’t a reliable predictor of cloud cover.

### Wind Speed vs. Latitude 
**Northern Hemisphere Linear Regression**

![Wind Speed vs  Latitude Linear Regression Plot Northern](https://github.com/user-attachments/assets/268cc752-c81c-40f4-8bfe-42391ce64dba)

- R-value: -0.04787380688942356
  
**Southern Hemisphere Linear Regression**

![Wind Speed vs  Latitude Linear Regression Plot Southern](https://github.com/user-attachments/assets/ac2019d5-2cce-4861-a68d-671e2d7c0fc1)

- R-value: -0.16650300888267477
  
**Key Insights: Wind Speed vs. Latitude** 

- There is no strong connection between latitude and wind speed. In the Northern Hemisphere, wind speeds tend to slightly decrease as you move north, while in the Southern Hemisphere, they increase slightly toward the South Pole. However, these trends are weak, meaning other factors play a bigger role in wind patterns.

- Wind speed is more influenced by factors like storms, pressure systems, and geographical features such as mountains and coastlines. The scattered data points, especially in the Northern Hemisphere, suggest that extreme wind speeds in some regions may be outliers rather than part of a clear trend.

## Challenges
- **Data Inconsistencies:** While using real-time weather data from the OpenWeatherMap API, some cities provided inconsistent or incomplete weather attributes.
- **Geographic Distribution:** The random city selection via latitude and longitude may not have perfectly captured cities across a wide range of climates.
- **Linear Regression Limitations:** Although linear regression provided some insights, it may not have fully captured the complexities of weather patterns, particularly with weak correlations between latitude and weather attributes. 

## Future Improvements
- **Advanced Weather Models:** Rather than using basic linear regression, more advanced statistical techniques or machine learning models could be applied to better understand the relationships between latitude and weather variables.
- **Seasonal Considerations:** Weather patterns are influenced by seasonal changes, and this analysis could be expanded to incorporate data from different times of the year to account for seasonal variation.
- **Enhanced Data Visualization:** While scatter plots provided valuable insights, using interactive visualizations with tools like Plotly or Dash could help users explore data trends more effectively.

## Conclusion
The project successfully explored the relationship between latitude and key weather attributes such as temperature, humidity, cloudiness, and wind speed. Although the analysis revealed some interesting trends, particularly regarding temperature and latitude, other factors such as altitude, ocean currents, and geographical features play significant roles in shaping weather patterns. The results showed that temperature is strongly influenced by latitude, while humidity, cloudiness, and wind speed have weaker correlations with latitude.
