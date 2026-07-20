# Add Order Product with BaseLinker

Adds a product to an order in BaseLinker.

## Endpoint

- **Method:** `POST`
- **Path:** `/connector.php`
- **Base URL:** `https://api.baselinker.com`
- **Official documentation:** [Add Order Product](https://api.baselinker.com/index.php?method=addOrderProduct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | body | `number` | yes | Order identifier to append a product to. |
| `storage` | body | `string` | no | Inventory source code for the product. |
| `storage_id` | body | `number` | no | Inventory source identifier for the product. |
| `product_id` | body | `number` | no | Product identifier from the selected storage. |
| `variant_id` | body | `number` | no | Variant identifier from the selected product. |
| `name` | body | `string` | no | Product name to add to the order. |
| `price_brutto` | body | `number` | no | Gross item price. |
| `quantity` | body | `number` | no | Quantity to add to the order. |
| `tax_rate` | body | `number` | no | VAT rate percentage for the item. |
| `attributes` | body | `object` | no | Product attributes payload for the order item. |
| `parameters` | body | `object` | no | Optional raw BaseLinker parameters merged with the typed fields before request serialization. |
