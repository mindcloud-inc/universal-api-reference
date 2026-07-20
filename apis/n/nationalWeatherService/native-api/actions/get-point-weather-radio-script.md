# Get Point Weather Radio Script with National Weather Service

Retrieves the weather radio script for a National Weather Service point.

## Endpoint

- **Method:** `GET`
- **Path:** `/points/:latitude,:longitude/radio`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [Get Point Weather Radio Script](https://api.weather.gov/openapi.json#/paths/~1points~1{latitude},{longitude}~1radio/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | path | `string` | no | Latitude in decimal degrees. |
| `longitude` | path | `string` | no | Longitude in decimal degrees. |
