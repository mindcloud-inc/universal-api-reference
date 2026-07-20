# Update Weather Station with OpenWeather

Updates a weather station in your OpenWeather account.

## Endpoint

- **Method:** `PUT`
- **Path:** `/data/3.0/stations/:stationId`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Update Weather Station](https://openweathermap.org/stations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stationId` | path | `string` | yes | Internal weather station identifier. |
| `external_id` | body | `string` | no | Updated external identifier for the station. |
| `name` | body | `string` | no | Updated station display name. |
| `latitude` | body | `number` | no | Updated station latitude. |
| `longitude` | body | `number` | no | Updated station longitude. |
| `altitude` | body | `number` | no | Updated station altitude in meters. |
