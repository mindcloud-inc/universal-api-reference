# Resolve Point Metadata with National Weather Service

Retrieves point metadata from National Weather Service by coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/points/:latitude,:longitude`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [Resolve Point Metadata](https://api.weather.gov/openapi.json#/paths/~1points~1{latitude},{longitude}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | path | `number` | yes | Latitude in decimal degrees. |
| `longitude` | path | `number` | yes | Longitude in decimal degrees. |
