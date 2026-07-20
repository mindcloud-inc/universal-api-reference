# Get Statistical Weather by Day with OpenWeather

Retrieves daily weather statistics from OpenWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `https://history.openweathermap.org/data/2.5/aggregated/day`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Statistical Weather by Day](https://old.openweathermap.org/api/statistics-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude of the location. |
| `lon` | query | `number` | yes | Longitude of the location. |
| `month` | query | `number` | yes | Month number for aggregation. |
| `day` | query | `number` | yes | Day of month for aggregation. |
