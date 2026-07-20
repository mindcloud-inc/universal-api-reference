# Geocode ZIP Code with OpenWeather

Finds an OpenWeather location by ZIP code.

## Endpoint

- **Method:** `GET`
- **Path:** `/geo/1.0/zip`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Geocode ZIP Code](https://openweathermap.org/api/geocoding-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `zip` | query | `string` | yes | ZIP or postal code with country code. |
