# Update order item with WeForest

Updates an existing tree-planting order item in WeForest.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/trees/:orderId/items/:itemId`
- **Base URL:** `https://api.weforest.org`
- **Official documentation:** [Update order item](https://docs.weforest.org/update-order-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `number` | yes | Order identifier from WeForest. |
| `itemId` | path | `number` | yes | Order item identifier from WeForest. |
| `quantity` | body | `number<object>` | yes | Updated quantity for this order item. |
