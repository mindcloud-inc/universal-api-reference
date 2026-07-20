# Retrieve Latest Pollen By Coordinates with Ambee

Retrieves latest pollen data in Ambee by coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/latest/pollen/by-lat-lng`
- **Base URL:** `https://api.ambeedata.com`
- **Official documentation:** [Retrieve Latest Pollen By Coordinates](https://docs.ambeedata.com/apis/pollen#latest-geospatial)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `lat` | query | `number` | yes |
| `lng` | query | `number` | yes |
