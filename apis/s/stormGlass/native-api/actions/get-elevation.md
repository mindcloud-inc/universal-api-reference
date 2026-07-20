# Get Elevation with Storm Glass

Retrieves elevation data from Storm Glass.

## Endpoint

- **Method:** `GET`
- **Path:** `/elevation/point`
- **Base URL:** `https://api.stormglass.io/v2`
- **Official documentation:** [Get Elevation](https://docs.stormglass.io/elevation.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude of the desired coordinate in decimal degrees. |
| `lng` | query | `number` | yes | Longitude of the desired coordinate in decimal degrees. |
