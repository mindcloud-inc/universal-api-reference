# Manage Product Prices with Freshworks CRM

Updates product prices in Freshworks CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/cpq/products/:id`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Manage Product Prices](https://developers.freshworks.com/crm/api/#add_prices_to_the_product)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `product` | body | `object` | yes |
| `product.product_pricings[]` | body | `array<object>` | yes |
| `product.product_pricings[].currency_code` | body | `string` | yes |
| `product.product_pricings[].currency_value` | body | `number` | yes |
