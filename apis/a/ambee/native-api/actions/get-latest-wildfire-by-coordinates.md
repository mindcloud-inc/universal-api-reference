# Get Latest Wildfire By Coordinates with Ambee

Retrieves latest wildfire data in Ambee by coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/fire/latest/by-lat-lng`
- **Base URL:** `https://api.ambeedata.com`
- **Official documentation:** [Get Latest Wildfire By Coordinates](https://docs.ambeedata.com/apis/fire#latest-geospatial)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `lat` | query | `number` | yes |
| `lng` | query | `number` | yes |
