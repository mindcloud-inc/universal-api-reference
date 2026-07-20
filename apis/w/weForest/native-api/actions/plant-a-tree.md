# Plant a tree with WeForest

Creates a new tree-planting request in WeForest.

## Endpoint

- **Method:** `POST`
- **Path:** `/trees`
- **Base URL:** `https://api.weforest.org`
- **Official documentation:** [Plant a tree](https://docs.weforest.org/plant-a-tree)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `items[]` | body | `array<object>` | yes | Array of order items with productId and quantity. |
| `sandbox` | body | `boolean` | no | Whether the order should be treated as a sandbox order. |
| `user` | body | `object` | no | End-user object for the order. |
