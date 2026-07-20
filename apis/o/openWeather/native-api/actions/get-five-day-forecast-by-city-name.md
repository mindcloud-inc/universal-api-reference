# Get 5 Day Forecast by City Name with OpenWeather

Retrieves a 5-day forecast from OpenWeather by city name.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/2.5/forecast`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get 5 Day Forecast by City Name](https://openweathermap.org/forecast5)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | City name, optionally including state code and country code separated by commas. |
