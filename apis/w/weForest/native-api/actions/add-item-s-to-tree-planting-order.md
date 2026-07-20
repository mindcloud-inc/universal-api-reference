# Add item(s) to tree-planting order with WeForest

Adds items to a tree-planting order in WeForest.

## Endpoint

- **Method:** `POST`
- **Path:** `/trees/:id/items`
- **Base URL:** `https://api.weforest.org`
- **Official documentation:** [Add item(s) to tree-planting order](https://docs.weforest.org/add-item-s-to-tree-planting-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Tree-planting request identifier from WeForest. |
| `items[]` | body | `array<object>` | yes | Array of order items with productId and quantity. |
