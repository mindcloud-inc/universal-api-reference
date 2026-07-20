# Get Hourly Forecast with Pirate Weather

Retrieves an hourly forecast from Pirate Weather.

## Endpoint

- **Method:** `GET`
- **Path:** `/forecast/header-auth/:latitude,:longitude`
- **Base URL:** `https://api.pirateweather.net`
- **Official documentation:** [Get Hourly Forecast](https://docs.pirateweather.net/en/latest/API/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | path | `number` | yes | Latitude in decimal degrees. |
| `longitude` | path | `number` | yes | Longitude in decimal degrees. |
