# Create Product with Dukaan

Creates a new product in Dukaan.

## Endpoint

- **Method:** `POST`
- **Path:** `api/product/seller/:storeUuid/product/v2/`
- **Base URL:** `https://api.mydukaan.io`
- **Official documentation:** [Create Product](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `storeUuid` | path | `string` | yes | Dukaan store UUID from developer settings. |
| `name` | body | `string` | yes | Product name. |
| `selling_price` | body | `number` | yes | Product selling price. |
| `original_price` | body | `number` | no | Product original price. |
| `unit` | body | `string` | no | Product unit. |
| `base_qty` | body | `number` | no | Base quantity for the product. |
| `description` | body | `string` | no | Product description HTML. |
| `categories[]` | body | `array<number>` | no | Category IDs for the product. |
| `store` | body | `string` | yes | Store UUID for the product body. |
| `sku_code` | body | `string` | no | Product SKU code. |
| `inventory_quantity` | body | `number` | no | Total product inventory quantity. |
| `in_stock` | body | `boolean` | no | Whether the product is in stock. |
