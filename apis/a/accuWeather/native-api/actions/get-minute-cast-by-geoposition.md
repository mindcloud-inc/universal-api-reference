# Get MinuteCast By Geoposition with AccuWeather

Retrieves MinuteCast data from AccuWeather by geoposition.

## Endpoint

- **Method:** `GET`
- **Path:** `/forecasts/v1/minute`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Get MinuteCast By Geoposition](https://developer.accuweather.com/minutecast)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Required geoposition as latitude,longitude. |
