# Get Current Weather by City Name with OpenWeather

Retrieves current weather from OpenWeather by city name.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/2.5/weather`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Current Weather by City Name](https://openweathermap.org/current)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | City name, optionally including state code and country code separated by commas. |
