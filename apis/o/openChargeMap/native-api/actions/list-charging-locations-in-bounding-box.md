# List Charging Locations In Bounding Box with Open Charge Map

## Endpoint

- **Method:** `GET`
- **Path:** `/poi`
- **Base URL:** `https://api.openchargemap.io/v3`
- **Official documentation:** [List Charging Locations In Bounding Box](https://www.openchargemap.org/develop/api#/operations/get-poi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `boundingbox` | query | `string` | yes | Bounding box as top-left and bottom-right corners: (lat,lng),(lat2,lng2). |
