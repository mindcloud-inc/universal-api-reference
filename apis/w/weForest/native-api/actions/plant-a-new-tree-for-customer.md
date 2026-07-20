# Plant a new tree for customer with WeForest

Creates a new tree for a customer in WeForest.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/:id/trees`
- **Base URL:** `https://api.weforest.org`
- **Official documentation:** [Plant a new tree for customer](https://docs.weforest.org/plant-a-new-tree-for-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Customer identifier from WeForest. |
| `items[]` | body | `array<object>` | yes | Array of order items with productId and quantity. |
