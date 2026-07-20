# Get Gridpoint Hourly Forecast with National Weather Service

Retrieves the hourly forecast for a National Weather Service gridpoint.

## Endpoint

- **Method:** `GET`
- **Path:** `/gridpoints/:wfo/:x,:y/forecast/hourly`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [Get Gridpoint Hourly Forecast](https://api.weather.gov/openapi.json#/paths/~1gridpoints~1{wfo}~1{x},{y}~1forecast~1hourly/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `wfo` | path | `string` | no | Weather Forecast Office identifier. |
| `x` | path | `string` | no | Gridpoint X coordinate. |
| `y` | path | `string` | no | Gridpoint Y coordinate. |
