# List Published Items with Qlik

Retrieves published copies of an item in Qlik.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/items/:itemId/publisheditems`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [List Published Items](https://qlik.dev/apis/rest/items/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemId` | path | `string` | yes | Qlik item ID. |
