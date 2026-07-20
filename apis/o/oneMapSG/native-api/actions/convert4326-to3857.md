# Convert WGS84 to EPSG:3857 with OneMap SG

Converts WGS84 coordinates to EPSG:3857 in OneMap SG.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/common/convert/4326to3857`
- **Base URL:** `https://www.onemap.gov.sg`
- **Official documentation:** [Convert WGS84 to EPSG:3857](https://www.onemap.gov.sg/apidocs/coordinate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | query | `number` | yes | The WGS84 latitude value. |
| `longitude` | query | `number` | yes | The WGS84 longitude value. |
