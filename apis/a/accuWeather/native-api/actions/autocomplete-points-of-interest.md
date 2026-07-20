# Autocomplete Points Of Interest with AccuWeather

Finds points of interest in AccuWeather by autocomplete.

## Endpoint

- **Method:** `GET`
- **Path:** `/locations/v1/pois/autocomplete`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Autocomplete Points Of Interest](https://developer.accuweather.com/core-weather/autocomplete-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Required autocomplete query text. |
