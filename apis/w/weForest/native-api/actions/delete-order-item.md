# Delete order item with WeForest

Deletes an existing tree-planting order item from WeForest.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/trees/:orderId/items/:itemId`
- **Base URL:** `https://api.weforest.org`
- **Official documentation:** [Delete order item](https://docs.weforest.org/delete-order-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `number` | yes | Order identifier from WeForest. |
| `itemId` | path | `number` | yes | Order item identifier from WeForest. |
