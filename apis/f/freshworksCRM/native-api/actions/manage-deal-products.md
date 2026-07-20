# Manage Deal Products with Freshworks CRM

Updates products on a deal in Freshworks CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/deals/:id`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Manage Deal Products](https://developers.freshworks.com/crm/api/#add_products_to_the_deal)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `products[]` | body | `array<object>` | no |
| `products[].id` | body | `number` | no |
| `products[].quantity` | body | `number` | no |
