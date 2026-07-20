# Convert WGS84 to SVY21 with OneMap SG

Converts WGS84 coordinates to SVY21 in OneMap SG.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/common/convert/4326to3414`
- **Base URL:** `https://www.onemap.gov.sg`
- **Official documentation:** [Convert WGS84 to SVY21](https://www.onemap.gov.sg/apidocs/coordinate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | query | `number` | yes | The WGS84 latitude value. |
| `longitude` | query | `number` | yes | The WGS84 longitude value. |
