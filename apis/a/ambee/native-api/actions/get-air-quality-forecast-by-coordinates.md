# Get Air Quality Forecast By Coordinates with Ambee

Retrieves air quality forecasts in Ambee by coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/forecast/aq/by-lat-lng`
- **Base URL:** `https://api.ambeedata.com`
- **Official documentation:** [Get Air Quality Forecast By Coordinates](https://docs.ambeedata.com/apis/air-quality#forecast-geospatial)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `lat` | query | `number` | yes |
| `lng` | query | `number` | yes |
