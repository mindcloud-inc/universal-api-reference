# List Countries By Region with AccuWeather

Lists the countries in AccuWeather for a region.

## Endpoint

- **Method:** `GET`
- **Path:** `/locations/v1/countries/:regionCode`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [List Countries By Region](https://developer.accuweather.com/accuweather-locations-api/apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `regionCode` | path | `string` | yes | Required AccuWeather region code. |
