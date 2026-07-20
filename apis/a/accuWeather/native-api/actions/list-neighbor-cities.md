# List Neighbor Cities with AccuWeather

Lists neighboring cities in AccuWeather for a location.

## Endpoint

- **Method:** `GET`
- **Path:** `/locations/v1/cities/neighbors/:locationKey`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [List Neighbor Cities](https://developer.accuweather.com/accuweather-locations-api/apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationKey` | path | `string` | yes | Required AccuWeather location key. |
