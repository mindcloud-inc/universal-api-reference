# Delete Weather Station with OpenWeather

Deletes a weather station from your OpenWeather account.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/data/3.0/stations/:stationId`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Delete Weather Station](https://openweathermap.org/stations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stationId` | path | `string` | yes | Internal weather station identifier. |
