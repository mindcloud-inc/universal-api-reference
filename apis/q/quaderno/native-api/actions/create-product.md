# Create Product with Quaderno

Creates a new product in Quaderno.

## Endpoint

- **Method:** `POST`
- **Path:** `/items`
- **Base URL:** `https://sandbox-quadernoapp.com/api`
- **Official documentation:** [Create Product](https://developers.quaderno.io/api/#tag/Products/operation/createProduct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | no | Product code. |
| `description` | body | `string` | no | Product description. |
| `kind` | body | `string` | no | Whether the product is one-off or subscription. |
| `name` | body | `string` | no | Product name. |
| `product_type` | body | `string` | no | Whether the product is a good or service. |
| `stock` | body | `string` | no | Available stock quantity. |
| `tax_based_on` | body | `string` | no | Whether tax is based on customer country or product country. |
| `tax_class` | body | `string` | no | Tax class for the product. |
| `tax_type` | body | `string` | no | Whether tax is included or excluded. |
| `unit_cost` | body | `string` | no | Unit cost for the product. |
