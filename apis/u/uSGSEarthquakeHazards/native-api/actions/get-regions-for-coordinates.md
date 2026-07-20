# Get Regions For Coordinates with USGS Earthquake Hazards

Retrieves regions for latitude and longitude coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/ws/geoserve/regions.json`
- **Base URL:** `https://earthquake.usgs.gov`
- **Official documentation:** [Get Regions For Coordinates](https://earthquake.usgs.gov/ws/geoserve/regions.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | query | `number` | yes | Latitude in decimal degrees of the point to look up. |
| `longitude` | query | `number` | yes | Longitude in decimal degrees of the point to look up. |
| `includeGeometry` | query | `boolean` | no | Set true to include polygon points for selected regions. |
| `type` | query | `string` | no | Comma-separated Geoserve region types to return. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
