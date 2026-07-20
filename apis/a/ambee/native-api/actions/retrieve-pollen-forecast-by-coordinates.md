# Retrieve Pollen Forecast By Coordinates with Ambee

Retrieves pollen forecasts in Ambee by coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/forecast/pollen/by-lat-lng`
- **Base URL:** `https://api.ambeedata.com`
- **Official documentation:** [Retrieve Pollen Forecast By Coordinates](https://docs.ambeedata.com/apis/pollen#forecast-geospatial)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `lat` | query | `number` | yes |
| `lng` | query | `number` | yes |
