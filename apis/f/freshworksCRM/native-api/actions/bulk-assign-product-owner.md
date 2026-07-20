# Bulk Assign Product Owner with Freshworks CRM

Updates product owners in Freshworks CRM in bulk.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/cpq/products/products_bulk_assign`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Bulk Assign Product Owner](https://developers.freshworks.com/crm/api/#bulk_assign_product_owner)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `owner_id` | body | `number` | yes |
| `selected_ids[]` | body | `array<number>` | yes |
