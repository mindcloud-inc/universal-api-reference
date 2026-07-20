# Get Daily Forecast by City Name with OpenWeather

Retrieves a daily forecast from OpenWeather by city name.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/2.5/forecast/daily`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Daily Forecast by City Name](https://openweathermap.org/forecast16)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | City name, optionally including state code and country code separated by commas. |
