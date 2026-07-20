# Create Product with Freshworks CRM

Creates a new product in Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/cpq/products`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Create Product](https://developers.freshworks.com/crm/api/#create_product)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `product` | body | `object` | yes |
| `product.base_currency_value` | body | `number` | no |
| `product.currency_value` | body | `number` | no |
| `product.description` | body | `string` | no |
| `product.display_name` | body | `string` | no |
| `product.name` | body | `string` | yes |
| `product.unit_price` | body | `number` | no |
