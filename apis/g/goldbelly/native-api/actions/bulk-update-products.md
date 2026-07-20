# Bulk Update Products with Goldbelly

## Endpoint

- **Method:** `POST`
- **Path:** `products/bulk_update`
- **Base URL:** `https://api.goldbelly.com/v1/`
- **Official documentation:** [Bulk Update Products](https://drive.google.com/file/d/1vH97uUnbEu3v2rs8JrZRi4oNAdp_uqWd/view?usp=sharing#products_bulk_update_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `products[]` | body | `array<object>` | yes | Products to update. Each item must include SKU and name; price and inventory are optional. |
| `products[].sku` | body | `string` | yes | Product SKU. |
| `products[].name` | body | `string` | yes | Product name. |
| `products[].price` | body | `number` | no | Product price. |
| `products[].inventory` | body | `number` | no | Product inventory quantity. |
