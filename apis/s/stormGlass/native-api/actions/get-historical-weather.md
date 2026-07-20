# Get Historical Weather with Storm Glass

Retrieves historical weather data from Storm Glass.

## Endpoint

- **Method:** `GET`
- **Path:** `/historical/point`
- **Base URL:** `https://api.stormglass.io/v2`
- **Official documentation:** [Get Historical Weather](https://docs.stormglass.io/historical.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude of the desired coordinate in decimal degrees. |
| `lng` | query | `number` | yes | Longitude of the desired coordinate in decimal degrees. |
| `params` | query | `string` | yes | Comma-separated historical weather parameters to retrieve, such as airTemperature,windSpeed,waveHeight. |
| `start` | query | `string` | yes | UTC first hour as UNIX time or ISO time. Historical requests require a start and end window. |
| `end` | query | `string` | yes | UTC final hour as UNIX time or ISO time. Each historical response covers up to 10 days. |
| `source` | query | `string` | no | Optional source such as sg, ecmwf, ecmwf:era5, cmems, or cmems:gopaf. |
