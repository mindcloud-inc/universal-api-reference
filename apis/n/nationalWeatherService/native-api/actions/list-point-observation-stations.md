# List Point Observation Stations with National Weather Service

Retrieves observation stations for a National Weather Service point.

## Endpoint

- **Method:** `GET`
- **Path:** `/points/:latitude,:longitude/stations`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [List Point Observation Stations](https://api.weather.gov/openapi.json#/paths/~1points~1{latitude},{longitude}~1stations/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | path | `string` | no | Latitude in decimal degrees. |
| `longitude` | path | `string` | no | Longitude in decimal degrees. |
