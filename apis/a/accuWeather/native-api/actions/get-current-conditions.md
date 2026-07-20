# Get Current Conditions with AccuWeather

Retrieves current conditions from AccuWeather for a location.

## Endpoint

- **Method:** `GET`
- **Path:** `/currentconditions/v1/:locationKey`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Get Current Conditions](https://developer.accuweather.com/core-weather/location-key-current-conditions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationKey` | path | `string` | yes | Required AccuWeather location key. |
