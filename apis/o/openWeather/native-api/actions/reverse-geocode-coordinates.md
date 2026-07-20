# Reverse Geocode Coordinates with OpenWeather

Finds OpenWeather locations by geographic coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/geo/1.0/reverse`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Reverse Geocode Coordinates](https://openweathermap.org/api/geocoding-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude to reverse geocode. |
| `lon` | query | `number` | yes | Longitude to reverse geocode. |
| `limit` | query | `number` | no | Maximum number of nearby locations to return. |
