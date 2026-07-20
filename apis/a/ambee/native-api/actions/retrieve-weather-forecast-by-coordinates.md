# Retrieve Weather Forecast By Coordinates with Ambee

Retrieves weather forecasts in Ambee by coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/weather/forecast/by-lat-lng`
- **Base URL:** `https://api.ambeedata.com`
- **Official documentation:** [Retrieve Weather Forecast By Coordinates](https://docs.ambeedata.com/apis/weather#forecast-geospatial)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `lat` | query | `number` | yes |
| `lng` | query | `number` | yes |
