# Get Daily Forecast 1 Day with AccuWeather

Retrieves a 1-day daily forecast from AccuWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `/forecasts/v1/daily/1day/:locationKey`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Get Daily Forecast 1 Day](https://developer.accuweather.com/core-weather/location-key-daily)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationKey` | path | `string` | yes | Required AccuWeather location key. |
