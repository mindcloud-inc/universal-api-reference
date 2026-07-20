# Get Latest Air Quality By Coordinates with Ambee

Retrieves latest air quality data in Ambee by coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/latest/by-lat-lng`
- **Base URL:** `https://api.ambeedata.com`
- **Official documentation:** [Get Latest Air Quality By Coordinates](https://docs.ambeedata.com/apis/air-quality#latest-geospatial)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `lat` | query | `number` | yes |
| `lng` | query | `number` | yes |
