# Get order item with WeForest

Retrieves a tree-planting order item from WeForest.

## Endpoint

- **Method:** `GET`
- **Path:** `/trees/:orderId/items/:itemId`
- **Base URL:** `https://api.weforest.org`
- **Official documentation:** [Get order item](https://docs.weforest.org/get-order-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `number` | yes | Order identifier from WeForest. |
| `itemId` | path | `number` | yes | Order item identifier from WeForest. |
