# Search Cities By Country with AccuWeather

Finds cities in AccuWeather by country and text.

## Endpoint

- **Method:** `GET`
- **Path:** `/locations/v1/cities/:countryCode/search`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Search Cities By Country](https://developer.accuweather.com/accuweather-locations-api/apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `countryCode` | path | `string` | yes | Required AccuWeather country code. |
| `q` | query | `string` | yes | Required city search query text. |
