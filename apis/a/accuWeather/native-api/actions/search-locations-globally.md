# Search Locations Globally with AccuWeather

Finds locations in AccuWeather by global text search.

## Endpoint

- **Method:** `GET`
- **Path:** `/locations/v1/search`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Search Locations Globally](https://developer.accuweather.com/core-weather/text-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Required search query text. |
