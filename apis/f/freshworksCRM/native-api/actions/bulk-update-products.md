# Bulk Update Products with Freshworks CRM

Updates multiple products in Freshworks CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/cpq/products/products_bulk_update`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Bulk Update Products](https://developers.freshworks.com/crm/api/#bulk_update_products)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ids[]` | body | `array<number>` | yes |
| `product` | body | `object` | yes |
| `product.description` | body | `string` | no |
| `product.owner_id` | body | `number` | no |
