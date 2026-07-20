# Update Product with Freshworks CRM

Updates an existing product in Freshworks CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/cpq/products/:id`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Update Product](https://developers.freshworks.com/crm/api/#update_a_product)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `product` | body | `object` | yes |
| `product.base_currency_value` | body | `number` | no |
| `product.currency_value` | body | `number` | no |
| `product.description` | body | `string` | no |
| `product.display_name` | body | `string` | no |
| `product.name` | body | `string` | no |
| `product.unit_price` | body | `number` | no |
