# List Item Collections with Qlik

Retrieves the collections for an item in Qlik.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/items/:itemId/collections`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [List Item Collections](https://qlik.dev/apis/rest/items/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemId` | path | `string` | yes | Qlik item ID. |
