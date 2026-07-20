# List Top Cities with AccuWeather

Lists top cities in AccuWeather by group.

## Endpoint

- **Method:** `GET`
- **Path:** `/locations/v1/topcities/:group`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [List Top Cities](https://developer.accuweather.com/accuweather-locations-api/apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group` | path | `string` | yes | Required top-city group number. |
