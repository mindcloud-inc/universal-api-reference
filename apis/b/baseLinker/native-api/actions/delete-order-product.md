# Delete Order Product with BaseLinker

Deletes a product from an order in BaseLinker.

## Endpoint

- **Method:** `POST`
- **Path:** `/connector.php`
- **Base URL:** `https://api.baselinker.com`
- **Official documentation:** [Delete Order Product](https://api.baselinker.com/index.php?method=deleteOrderProduct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | body | `number` | yes | Order identifier. |
| `order_product_id` | body | `number` | yes | Order product line identifier to remove. |
