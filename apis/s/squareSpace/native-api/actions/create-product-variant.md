# Create Product Variant with SquareSpace

Creates a product variant in Squarespace.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/commerce/products/:id/variants`
- **Base URL:** `https://api.squarespace.com`
- **Official documentation:** [Create Product Variant](https://developers.squarespace.com/commerce-apis/products#create-product-variant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `list<string>` | yes | Product ID. |
| `pricing.basePrice.currency` | body | `string` | no | Variant base price currency (ISO code). |
| `pricing.basePrice.value` | body | `string` | no | Variant base price amount. |
| `sku` | body | `string` | yes | Variant SKU code. |
| `stock.quantity` | body | `number` | no | Finite stock quantity. |
| `stock.unlimited` | body | `boolean` | no | Whether stock is unlimited. |
