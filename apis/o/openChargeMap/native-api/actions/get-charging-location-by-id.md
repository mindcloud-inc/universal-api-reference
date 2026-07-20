# Get Charging Location By ID with Open Charge Map

## Endpoint

- **Method:** `GET`
- **Path:** `/poi`
- **Base URL:** `https://api.openchargemap.io/v3`
- **Official documentation:** [Get Charging Location By ID](https://www.openchargemap.org/develop/api#/operations/get-poi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chargepointid` | query | `string` | yes | Exact match on a given OCM POI ID. Comma-separated IDs are supported by Open Charge Map. |
