# Convert SVY21 to WGS84 with OneMap SG

Converts SVY21 coordinates to WGS84 in OneMap SG.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/common/convert/3414to4326`
- **Base URL:** `https://www.onemap.gov.sg`
- **Official documentation:** [Convert SVY21 to WGS84](https://www.onemap.gov.sg/apidocs/coordinate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `X` | query | `number` | yes | The SVY21 X coordinate. |
| `Y` | query | `number` | yes | The SVY21 Y coordinate. |
