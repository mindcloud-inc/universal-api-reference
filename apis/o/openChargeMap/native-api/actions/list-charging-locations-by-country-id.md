# List Charging Locations By Country ID with Open Charge Map

## Endpoint

- **Method:** `GET`
- **Path:** `/poi`
- **Base URL:** `https://api.openchargemap.io/v3`
- **Official documentation:** [List Charging Locations By Country ID](https://www.openchargemap.org/develop/api#/operations/get-poi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `countryid` | query | `string` | yes | Exact match on a numeric Open Charge Map country ID. Comma-separated IDs are supported. |
