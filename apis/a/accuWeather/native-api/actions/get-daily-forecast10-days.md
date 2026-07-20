# Get Daily Forecast 10 Days with AccuWeather

Retrieves a 10-day daily forecast from AccuWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `/forecasts/v1/daily/10day/:locationKey`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Get Daily Forecast 10 Days](https://developer.accuweather.com/core-weather/location-key-daily)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationKey` | path | `string` | yes | Required AccuWeather location key. |
