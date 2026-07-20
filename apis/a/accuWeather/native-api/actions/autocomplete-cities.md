# Autocomplete Cities with AccuWeather

Finds cities in AccuWeather by autocomplete text.

## Endpoint

- **Method:** `GET`
- **Path:** `/locations/v1/cities/autocomplete`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Autocomplete Cities](https://developer.accuweather.com/accuweather-locations-api/apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Required autocomplete query text. |
