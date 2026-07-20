# Get Location By Key with AccuWeather

Retrieves a location from AccuWeather by key.

## Endpoint

- **Method:** `GET`
- **Path:** `/locations/v1/:locationKey`
- **Base URL:** `https://dataservice.accuweather.com`
- **Official documentation:** [Get Location By Key](https://developer.accuweather.com/accuweather-locations-api/apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationKey` | path | `string` | yes | Required AccuWeather location key. |
