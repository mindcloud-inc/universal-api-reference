# Get Alarm 5 Days with AccuWeather

Retrieves 5-day weather alarms from AccuWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `/alarms/v1/5day/:locationKey`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Get Alarm 5 Days](https://developer.accuweather.com/core-weather/location-key-alarms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationKey` | path | `string` | yes | Required AccuWeather location key. |
