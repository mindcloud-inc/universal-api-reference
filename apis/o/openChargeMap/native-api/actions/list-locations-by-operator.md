# List Locations By Operator with Open Charge Map

## Endpoint

- **Method:** `GET`
- **Path:** `/poi`
- **Base URL:** `https://api.openchargemap.io/v3`
- **Official documentation:** [List Locations By Operator](https://www.openchargemap.org/develop/api#/operations/get-poi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `operatorid` | query | `string` | yes | Exact match on a given EVSE operator ID. Comma-separated IDs are supported. |
