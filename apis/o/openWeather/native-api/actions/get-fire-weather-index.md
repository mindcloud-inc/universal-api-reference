# Get Fire Weather Index with OpenWeather

Retrieves the fire weather index from OpenWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.openweathermap.org/data/2.5/fwi`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Fire Weather Index](https://openweathermap.org/api/fire-index-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `string` | yes | Latitude of the location. |
| `lon` | query | `string` | yes | Longitude of the location. |
