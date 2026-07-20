# Get 5 Day Indices Group with AccuWeather

Retrieves 5-day index groups from AccuWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `/indices/v1/daily/5day/:locationKey/groups/:ID`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Get 5 Day Indices Group](https://developer.accuweather.com/accuweather-indices-api/apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ID` | path | `string` | no | Required index group ID. |
| `locationKey` | path | `string` | no | Required AccuWeather location key. |
