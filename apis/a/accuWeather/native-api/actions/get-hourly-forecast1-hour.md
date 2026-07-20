# Get Hourly Forecast 1 Hour with AccuWeather

Retrieves a 1-hour hourly forecast from AccuWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `/forecasts/v1/hourly/1hour/:locationKey`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Get Hourly Forecast 1 Hour](https://developer.accuweather.com/core-weather/location-key-hourly)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationKey` | path | `string` | yes | Required AccuWeather location key. |
