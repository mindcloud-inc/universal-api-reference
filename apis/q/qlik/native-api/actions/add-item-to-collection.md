# Add Item To Collection with Qlik

Adds an item to a collection in Qlik.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/collections/:collectionId/items`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [Add Item To Collection](https://qlik.dev/apis/rest/collections/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | Qlik collection ID. |
| `id` | body | `string` | yes | Item ID to add to the collection. |
