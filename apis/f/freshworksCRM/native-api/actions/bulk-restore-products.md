# Bulk Restore Products with Freshworks CRM

Restores multiple products in Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/cpq/products/products_bulk_restore`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Bulk Restore Products](https://developers.freshworks.com/crm/api/#bulk_restore_products)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `selected_ids[]` | body | `array<number>` | yes |
