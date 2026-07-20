# Get Weather Alerts with AccuWeather

Retrieves weather alerts from AccuWeather for a location.

## Endpoint

- **Method:** `GET`
- **Path:** `/alerts/v1/:locationKey`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Get Weather Alerts](https://developer.accuweather.com/core-weather/weather-alerts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationKey` | path | `string` | yes | Required AccuWeather location key. |
