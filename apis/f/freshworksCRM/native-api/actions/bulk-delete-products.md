# Bulk Delete Products with Freshworks CRM

Deletes multiple products from Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/cpq/products/products_bulk_delete`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Bulk Delete Products](https://developers.freshworks.com/crm/api/#bulk_delete_products)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `selected_ids[]` | body | `array<number>` | yes |
