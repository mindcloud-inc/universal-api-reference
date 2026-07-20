# Get Current Weather with OpenWeather

Retrieves current weather from OpenWeather by coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/2.5/weather`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Current Weather](https://openweathermap.org/current)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude of the location to fetch weather for. |
| `lon` | query | `number` | yes | Longitude of the location to fetch weather for. |
| `units` | query | `string` | no | Units to use for temperature and wind speed. Accepted values: `0`, `1`, `2`. |
| `lang` | query | `string` | no | Language code for weather condition descriptions. |
