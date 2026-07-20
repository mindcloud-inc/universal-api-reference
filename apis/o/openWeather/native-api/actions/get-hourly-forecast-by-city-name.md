# Get Hourly Forecast by City Name with OpenWeather

Retrieves an hourly forecast from OpenWeather by city name.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/2.5/forecast/hourly`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Hourly Forecast by City Name](https://openweathermap.org/api/hourly-forecast)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | City name, optionally including state code and country code separated by commas. |
