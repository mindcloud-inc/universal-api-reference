# List Locations By Connection Type with Open Charge Map

## Endpoint

- **Method:** `GET`
- **Path:** `/poi`
- **Base URL:** `https://api.openchargemap.io/v3`
- **Official documentation:** [List Locations By Connection Type](https://www.openchargemap.org/develop/api#/operations/get-poi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connectiontypeid` | query | `string` | yes | Exact match on a connection type ID. Comma-separated IDs are supported. |
