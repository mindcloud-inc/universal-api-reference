# Get Forecast with Pirate Weather

Retrieves a weather forecast from Pirate Weather.

## Endpoint

- **Method:** `GET`
- **Path:** `/forecast/header-auth/:latitude,:longitude`
- **Base URL:** `https://api.pirateweather.net`
- **Official documentation:** [Get Forecast](https://docs.pirateweather.net/en/latest/API/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | path | `number` | yes | Latitude in decimal degrees, for example 45.42. |
| `longitude` | path | `number` | yes | Longitude in decimal degrees, for example -75.69. |
