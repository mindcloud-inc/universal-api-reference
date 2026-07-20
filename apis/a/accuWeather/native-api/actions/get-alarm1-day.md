# Get Alarm 1 Day with AccuWeather

Retrieves 1-day weather alarms from AccuWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `/alarms/v1/1day/:locationKey`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Get Alarm 1 Day](https://developer.accuweather.com/core-weather/location-key-alarms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationKey` | path | `string` | yes | Required AccuWeather location key. |
