# Retrieve Pollen 120hr Forecast By Coordinates with Ambee

Retrieves 120-hour pollen forecasts in Ambee by coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/forecast/v2/pollen/120hr/by-lat-lng`
- **Base URL:** `https://api.ambeedata.com`
- **Official documentation:** [Retrieve Pollen 120hr Forecast By Coordinates](https://docs.ambeedata.com/apis/pollen#forecast-geospatial-120hr)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `lat` | query | `number` | yes |
| `lng` | query | `number` | yes |
