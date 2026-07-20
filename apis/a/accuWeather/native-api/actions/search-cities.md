# Search Cities with AccuWeather

Finds cities in AccuWeather by text search.

## Endpoint

- **Method:** `GET`
- **Path:** `/locations/v1/cities/search`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Search Cities](https://developer.accuweather.com/accuweather-locations-api/apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Required city search query text. |
