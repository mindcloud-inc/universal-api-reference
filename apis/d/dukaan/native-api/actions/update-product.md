# Update Product with Dukaan

Updates an existing product in Dukaan.

## Endpoint

- **Method:** `PATCH`
- **Path:** `api/product/seller/:storeUuid/product/:productUuid/v2/`
- **Base URL:** `https://api.mydukaan.io`
- **Official documentation:** [Update Product](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `storeUuid` | path | `string` | yes | Dukaan store UUID from developer settings. |
| `productUuid` | path | `string` | yes | Dukaan product UUID. |
| `name` | body | `string` | no | Product name. |
| `selling_price` | body | `number` | no | Product selling price. |
| `original_price` | body | `number` | no | Product original price. |
| `description` | body | `string` | no | Product description HTML. |
| `categories[]` | body | `array<number>` | no | Category IDs for the product. |
| `skus[]` | body | `array<object>` | no | SKU objects for product variants. |
| `in_stock` | body | `boolean` | no | Whether the product is in stock. |
