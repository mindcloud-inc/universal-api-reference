# Search Admin Areas By Country with AccuWeather

Finds admin areas in AccuWeather by country.

## Endpoint

- **Method:** `GET`
- **Path:** `/locations/v1/adminareas/:countryCode/search`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Search Admin Areas By Country](https://developer.accuweather.com/core-weather/text-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `countryCode` | path | `string` | yes | Required AccuWeather country code. |
| `q` | query | `string` | yes | Required search query text. |
