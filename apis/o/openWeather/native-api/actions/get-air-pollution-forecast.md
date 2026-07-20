# Get Air Pollution Forecast with OpenWeather

Retrieves an air pollution forecast from OpenWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/2.5/air_pollution/forecast`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Air Pollution Forecast](https://openweathermap.org/api/air-pollution)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude of the location. |
| `lon` | query | `number` | yes | Longitude of the location. |
