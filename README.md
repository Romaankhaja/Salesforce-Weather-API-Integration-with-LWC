Salesforce Weather Details Apex Integration
Overview
This repository contains an Apex class for Salesforce that integrates with the OpenWeatherMap API to fetch and display current weather details for a given city. The provided WeatherDetailsClass is designed to be used within Salesforce Lightning Web Components (LWC) or other Apex-driven processes to retrieve and present weather information.

Features
API Integration: Connects to the OpenWeatherMap API to get current weather data.
Weather Details Retrieval: Fetches and parses weather information including temperature, pressure, humidity, and more.
Wrapper Class: Encapsulates the weather details in a structured format for easy use in Salesforce.
Key Components
WeatherDetailsClass: Apex class responsible for making HTTP callouts to the weather API, processing the response, and returning weather details.
WeatherDetailsWrapper: Inner class used to format and store the weather information.
Code Breakdown
getWeatherDetails(String cityName)
Purpose: Retrieves weather details for a specified city.
Parameters: cityName - Name of the city to fetch weather data for.
Process:
Constructs the API endpoint URL with the city name and API key.
Makes an HTTP GET request to the OpenWeatherMap API.
Processes the API response and maps it to a WeatherDetailsWrapper instance.
Returns the weather details encapsulated in the wrapper class.
WeatherDetailsWrapper
Purpose: Holds the weather data in a structured manner.
Attributes:
city: City name.
temperature: Current temperature.
pressure: Atmospheric pressure.
humidity: Humidity percentage.
feelsLike: Feels-like temperature.
tempMin: Minimum temperature.
tempMax: Maximum temperature.
