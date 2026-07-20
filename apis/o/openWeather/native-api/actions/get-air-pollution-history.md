# Get Air Pollution History with OpenWeather

Retrieves air pollution history from OpenWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/2.5/air_pollution/history`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Air Pollution History](https://openweathermap.org/api/air-pollution)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude of the location. |
| `lon` | query | `number` | yes | Longitude of the location. |
| `start` | query | `number` | yes | Unix timestamp for the start of the historical interval. |
| `end` | query | `number` | yes | Unix timestamp for the end of the historical interval. |
