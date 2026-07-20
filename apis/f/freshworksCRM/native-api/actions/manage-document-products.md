# Manage Document Products with Freshworks CRM

Updates products on a document in Freshworks CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/cpq/cpq_documents/:id`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Manage Document Products](https://developers.freshworks.com/crm/api/#add_products_to_the_document)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `products[]` | body | `array<object>` | no |
| `products[].id` | body | `number` | no |
| `products[].quantity` | body | `number` | no |
