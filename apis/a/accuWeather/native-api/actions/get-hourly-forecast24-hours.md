# Get Hourly Forecast 24 Hours with AccuWeather

Retrieves a 24-hour hourly forecast from AccuWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `/forecasts/v1/hourly/24hour/:locationKey`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Get Hourly Forecast 24 Hours](https://developer.accuweather.com/core-weather/location-key-hourly)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationKey` | path | `string` | yes | Required AccuWeather location key. |
