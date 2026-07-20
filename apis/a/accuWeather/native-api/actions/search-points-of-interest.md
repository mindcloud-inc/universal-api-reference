# Search Points Of Interest with AccuWeather

Finds points of interest in AccuWeather by text.

## Endpoint

- **Method:** `GET`
- **Path:** `/locations/v1/pois/search`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Search Points Of Interest](https://developer.accuweather.com/core-weather/point-of-interest-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Required point of interest query text. |
