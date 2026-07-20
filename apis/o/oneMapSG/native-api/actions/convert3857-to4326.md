# Convert EPSG:3857 to WGS84 with OneMap SG

Converts EPSG:3857 coordinates to WGS84 in OneMap SG.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/common/convert/3857to4326`
- **Base URL:** `https://www.onemap.gov.sg`
- **Official documentation:** [Convert EPSG:3857 to WGS84](https://www.onemap.gov.sg/apidocs/coordinate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `X` | query | `number` | yes | The EPSG:3857 X coordinate. |
| `Y` | query | `number` | yes | The EPSG:3857 Y coordinate. |
