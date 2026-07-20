# List Charging Locations In Polygon with Open Charge Map

## Endpoint

- **Method:** `GET`
- **Path:** `/poi`
- **Base URL:** `https://api.openchargemap.io/v3`
- **Official documentation:** [List Charging Locations In Polygon](https://www.openchargemap.org/develop/api#/operations/get-poi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `polygon` | query | `string` | yes | Encoded polyline polygon shape. Open Charge Map automatically closes the polygon. |
