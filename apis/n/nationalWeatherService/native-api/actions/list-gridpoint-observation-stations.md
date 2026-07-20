# List Gridpoint Observation Stations with National Weather Service

Retrieves observation stations for a National Weather Service gridpoint.

## Endpoint

- **Method:** `GET`
- **Path:** `/gridpoints/:wfo/:x,:y/stations`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [List Gridpoint Observation Stations](https://api.weather.gov/openapi.json#/paths/~1gridpoints~1{wfo}~1{x},{y}~1stations/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `wfo` | path | `string` | no | Weather Forecast Office identifier. |
| `x` | path | `string` | no | Gridpoint X coordinate. |
| `y` | path | `string` | no | Gridpoint Y coordinate. |
