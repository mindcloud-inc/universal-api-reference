# List Current Conditions For Top Cities with AccuWeather

Lists current conditions for top cities in AccuWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `/currentconditions/v1/topcities/:group`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [List Current Conditions For Top Cities](https://developer.accuweather.com/core-weather/top-cities-current-conditions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group` | path | `string` | yes | Required top-city group number. |
