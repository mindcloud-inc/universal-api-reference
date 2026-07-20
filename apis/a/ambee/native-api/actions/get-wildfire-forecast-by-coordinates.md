# Get Wildfire Forecast By Coordinates with Ambee

Retrieves wildfire risk forecasts in Ambee by coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/fire/risk/by-lat-lng`
- **Base URL:** `https://api.ambeedata.com`
- **Official documentation:** [Get Wildfire Forecast By Coordinates](https://docs.ambeedata.com/apis/fire#forecast-geospatial)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `lat` | query | `number` | yes |
| `lng` | query | `number` | yes |
