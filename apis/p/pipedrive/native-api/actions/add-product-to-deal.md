# Add Product to Deal with Pipedrive

Adds a product to a deal in Pipedrive.

## Endpoint

- **Method:** `POST`
- **Path:** `v2/deals/:dealId/products`
- **Base URL:** `{api_domain}/api`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `dealId` | path | `string` | yes |
| `product_id` | body | `number` | no |
| `item_price` | body | `number` | no |
| `quantity` | body | `number` | no |
| `comments` | body | `string` | no |
