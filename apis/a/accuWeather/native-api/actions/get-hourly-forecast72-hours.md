# Get Hourly Forecast 72 Hours with AccuWeather

Retrieves a 72-hour hourly forecast from AccuWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `/forecasts/v1/hourly/72hour/:locationKey`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Get Hourly Forecast 72 Hours](https://developer.accuweather.com/core-weather/location-key-hourly)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationKey` | path | `string` | yes | Required AccuWeather location key. |
