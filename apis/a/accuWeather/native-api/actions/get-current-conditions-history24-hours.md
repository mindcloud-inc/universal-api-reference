# Get Current Conditions History 24 Hours with AccuWeather

Retrieves 24-hour current conditions history from AccuWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `/currentconditions/v1/:locationKey/historical/24`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Get Current Conditions History 24 Hours](https://developer.accuweather.com/core-weather/24-hour-historical-current-conditions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationKey` | path | `string` | yes | Required AccuWeather location key. |
