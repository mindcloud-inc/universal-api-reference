# Get Current Conditions History 6 Hours with AccuWeather

Retrieves 6-hour current conditions history from AccuWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `/currentconditions/v1/:locationKey/historical`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Get Current Conditions History 6 Hours](https://developer.accuweather.com/core-weather/6-hour-historical-current-conditions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationKey` | path | `string` | yes | Required AccuWeather location key. |
