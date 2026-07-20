# Get Tropical Storm By Government Id with AccuWeather

Retrieves a tropical storm from AccuWeather by year, basin, and government ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/tropical/v1/gov/storms/:year/:basin/:govId`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Get Tropical Storm By Government Id](https://developer.accuweather.com/core-weather/active)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `basin` | path | `string` | yes | Required tropical basin code. |
| `govId` | path | `string` | yes | Required government storm ID. |
| `year` | path | `string` | yes | Required four-digit year. |
