# Get Statistical Weather by Month with OpenWeather

Retrieves monthly weather statistics from OpenWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `https://history.openweathermap.org/data/2.5/aggregated/month`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Statistical Weather by Month](https://old.openweathermap.org/api/statistics-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude of the location. |
| `lon` | query | `number` | yes | Longitude of the location. |
| `month` | query | `number` | yes | Month number for aggregation. |
| `year` | query | `number` | yes | Year for aggregation. |
