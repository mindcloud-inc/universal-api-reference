# Get Alarm 15 Days with AccuWeather

Retrieves 15-day weather alarms from AccuWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `/alarms/v1/15day/:locationKey`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Get Alarm 15 Days](https://developer.accuweather.com/core-weather/location-key-alarms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationKey` | path | `string` | yes | Required AccuWeather location key. |
