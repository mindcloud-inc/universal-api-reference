# Get Climatic Forecast by City Name with OpenWeather

Retrieves a 30-day climate forecast from OpenWeather by city name.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/2.5/forecast/climate`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Climatic Forecast by City Name](https://openweathermap.org/api/forecast30)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | City name, optionally including state code and country code separated by commas. |
