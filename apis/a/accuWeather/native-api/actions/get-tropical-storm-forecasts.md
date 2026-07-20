# Get Tropical Storm Forecasts with AccuWeather

Retrieves tropical storm forecasts from AccuWeather by year, basin, and government ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/tropical/v1/gov/storms/:year/:basin/:govId/forecasts`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Get Tropical Storm Forecasts](https://developer.accuweather.com/core-weather/forecast-tropical)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `basin` | path | `string` | yes | Required tropical basin code. |
| `govId` | path | `string` | yes | Required government storm ID. |
| `year` | path | `string` | yes | Required four-digit year. |
