# Search Cities By Country And Admin Area with AccuWeather

Finds cities in AccuWeather by country and admin area.

## Endpoint

- **Method:** `GET`
- **Path:** `/locations/v1/cities/:countryCode/:adminCode/search`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Search Cities By Country And Admin Area](https://developer.accuweather.com/accuweather-locations-api/apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adminCode` | path | `string` | yes | Required AccuWeather admin area code. |
| `countryCode` | path | `string` | yes | Required AccuWeather country code. |
| `q` | query | `string` | yes | Required city search query text. |
