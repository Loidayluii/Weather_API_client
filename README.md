#  Weather API App

A simple desktop weather application built with PyQt5 and the OpenWeatherMap API. 
Enter any city name and instantly get the current temperature, a weather emoji, and a short description.

## Features

-  Search weather by city name
-  Displays current temperature in Celsius
-  Weather condition shown as an emoji (sunny, rainy, snowy, stormy, foggy, cloudy, etc.)
-  Human-readable weather description
-  Friendly error messages for invalid cities, bad connections, timeouts, and API errors

## Tech Stack

- Python 3
- [PyQt5](https://pypi.org/project/PyQt5/) — GUI framework
- [Requests](https://pypi.org/project/requests/) — HTTP client
- [OpenWeatherMap API](https://openweathermap.org/api) — weather data source

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
```

### 2. Install dependencies

```bash
pip install PyQt5 requests
```

### 3. Add your OpenWeatherMap API key

Sign up for a free API key at [openweathermap.org/api](https://openweathermap.org/api), then paste it into the `api_key` variable in `weather_app.py`.

### 4. Run the app

```bash
python weather_app.py
```
## How It Works

1. The user types a city name and clicks **Get Weather**.
2. The app sends a request to the OpenWeatherMap API for that city.
3. The response is parsed for temperature, weather condition ID, and description.
4. The weather condition ID is mapped to an emoji (e.g. `800` → ☀️, `200–232` → ⛈️).
5. Results are displayed in the UI; any request errors are caught and shown as a friendly message.

## Possible Improvements

-  Add a 5-day forecast view
-  Support switching between °C and °F
-  Remember the last searched city
-  Add unit tests for the emoji-mapping logic
