# Get Current Air Pollution with OpenWeather

Retrieves current air pollution data from OpenWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/2.5/air_pollution`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Current Air Pollution](https://openweathermap.org/api/air-pollution)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude of the location. |
| `lon` | query | `number` | yes | Longitude of the location. |
