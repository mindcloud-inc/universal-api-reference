# List Collection Items with Qlik

Retrieves items from a collection in Qlik.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/collections/:collectionId/items`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [List Collection Items](https://qlik.dev/apis/rest/collections/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | Qlik collection ID. |
