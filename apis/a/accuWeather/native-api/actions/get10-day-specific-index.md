# Get 10 Day Specific Index with AccuWeather

Retrieves a 10-day specific index from AccuWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `/indices/v1/daily/10day/:locationKey/:ID`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Get 10 Day Specific Index](https://developer.accuweather.com/accuweather-indices-api/apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ID` | path | `string` | no | Required index ID. |
| `locationKey` | path | `string` | no | Required AccuWeather location key. |
