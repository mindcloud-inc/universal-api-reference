# Search Regions with AccuWeather

Retrieves a region from AccuWeather by region code.

## Endpoint

- **Method:** `GET`
- **Path:** `/locations/v1/regions/:regionCode`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Search Regions](https://developer.accuweather.com/core-weather/text-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `regionCode` | path | `string` | yes | Required AccuWeather region code. |
