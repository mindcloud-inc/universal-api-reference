# Get Aggregated Weather Station Measurements with OpenWeather

Retrieves aggregated weather station measurements from OpenWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/3.0/measurements`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Aggregated Weather Station Measurements](https://openweathermap.org/stations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `station_id` | query | `string` | yes | One or more station identifiers to filter measurements for. |
| `type` | query | `string` | yes | Aggregation type: hour, day, or month depending on provider support. |
| `from` | query | `number` | yes | Unix timestamp for the start of the aggregation window. |
| `to` | query | `number` | yes | Unix timestamp for the end of the aggregation window. |
