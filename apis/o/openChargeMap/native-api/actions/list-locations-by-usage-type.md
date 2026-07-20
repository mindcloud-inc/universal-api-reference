# List Locations By Usage Type with Open Charge Map

## Endpoint

- **Method:** `GET`
- **Path:** `/poi`
- **Base URL:** `https://api.openchargemap.io/v3`
- **Official documentation:** [List Locations By Usage Type](https://www.openchargemap.org/develop/api#/operations/get-poi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `usagetypeid` | query | `string` | yes | Exact match on a usage type ID. Comma-separated IDs are supported. |
