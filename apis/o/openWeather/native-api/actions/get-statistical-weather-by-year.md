# Get Statistical Weather by Year with OpenWeather

Retrieves yearly weather statistics from OpenWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `https://history.openweathermap.org/data/2.5/aggregated/year`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Statistical Weather by Year](https://old.openweathermap.org/api/statistics-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude of the location. |
| `lon` | query | `number` | yes | Longitude of the location. |
| `start` | query | `number` | yes | Start year for aggregation. |
| `end` | query | `number` | yes | End year for aggregation. |
