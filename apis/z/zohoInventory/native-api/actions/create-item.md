# Create Item with Zoho Inventory

Creates a new item in Zoho Inventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/items`
- **Base URL:** `{api_domain}/inventory/v1`
- **Official documentation:** [Create Item](https://www.zoho.com/inventory/api/v1/items/#create-an-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `string` | yes | Zoho Inventory organization ID to run this request against. |
| `name` | body | `string` | yes | Display name of the item. |
| `rate` | body | `number` | no | Sales rate for the item. |
| `description` | body | `string` | no | Description for the item. |
| `sku` | body | `string` | no | Stock keeping unit for the item. |
| `item_type` | body | `string` | no | Type of item to create. |
