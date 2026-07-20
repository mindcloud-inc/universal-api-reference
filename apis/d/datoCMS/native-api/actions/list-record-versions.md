# List Record Versions with DatoCMS

## Endpoint

- **Method:** `GET`
- **Path:** `/items/:item_id/versions`
- **Base URL:** `https://site-api.datocms.com`
- **Official documentation:** [List Record Versions](https://www.datocms.com/docs/content-management-api/resources/item-version/instances)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `item_id` | path | `string` | yes | — |
| `nested` | query | `boolean` | no | Return full nested block payloads instead of IDs. |
