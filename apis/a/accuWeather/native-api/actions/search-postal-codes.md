# Search Postal Codes with AccuWeather

Finds locations in AccuWeather by postal code.

## Endpoint

- **Method:** `GET`
- **Path:** `/locations/v1/postalcodes/search`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Search Postal Codes](https://developer.accuweather.com/core-weather/postal-code-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Required postal code text. |
