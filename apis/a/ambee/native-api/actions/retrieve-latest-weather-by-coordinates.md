# Retrieve Latest Weather By Coordinates with Ambee

Retrieves latest weather data in Ambee by coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/weather/latest/by-lat-lng`
- **Base URL:** `https://api.ambeedata.com`
- **Official documentation:** [Retrieve Latest Weather By Coordinates](https://docs.ambeedata.com/apis/weather#latest-geospatial)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `lat` | query | `number` | yes |
| `lng` | query | `number` | yes |
