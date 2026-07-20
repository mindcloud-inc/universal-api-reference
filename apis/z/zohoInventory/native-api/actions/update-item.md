# Update Item with Zoho Inventory

Updates an existing item in Zoho Inventory.

## Endpoint

- **Method:** `PUT`
- **Path:** `/items/:item_id`
- **Base URL:** `{api_domain}/inventory/v1`
- **Official documentation:** [Update Item](https://www.zoho.com/inventory/api/v1/items/#update-an-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `item_id` | path | `string` | yes | The Zoho Inventory item_id for the item. |
| `organization_id` | query | `string` | yes | Zoho Inventory organization ID to run this request against. |
| `name` | body | `string` | yes | Display name of the item. |
| `rate` | body | `number` | no | Sales rate for the item. |
| `description` | body | `string` | no | Description for the item. |
| `sku` | body | `string` | no | Stock keeping unit for the item. |
| `item_type` | body | `string` | no | Type of item to update. |
