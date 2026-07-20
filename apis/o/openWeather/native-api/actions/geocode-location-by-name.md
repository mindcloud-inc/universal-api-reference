# Geocode Location by Name with OpenWeather

Finds matching OpenWeather locations by name.

## Endpoint

- **Method:** `GET`
- **Path:** `/geo/1.0/direct`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Geocode Location by Name](https://openweathermap.org/api/geocoding-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Location name to geocode. |
| `limit` | query | `number` | no | Maximum number of matching locations to return. |
