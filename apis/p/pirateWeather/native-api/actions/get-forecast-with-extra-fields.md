# Get Forecast With Extra Fields with Pirate Weather

Retrieves a forecast with extra fields from Pirate Weather.

## Endpoint

- **Method:** `GET`
- **Path:** `/forecast/header-auth/:latitude,:longitude`
- **Base URL:** `https://api.pirateweather.net`
- **Official documentation:** [Get Forecast With Extra Fields](https://docs.pirateweather.net/en/latest/API/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | path | `number` | yes | Latitude in decimal degrees. |
| `longitude` | path | `number` | yes | Longitude in decimal degrees. |
