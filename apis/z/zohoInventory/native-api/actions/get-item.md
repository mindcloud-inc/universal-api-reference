# Get Item with Zoho Inventory

Retrieves an item from Zoho Inventory.

## Endpoint

- **Method:** `GET`
- **Path:** `/items/:item_id`
- **Base URL:** `{api_domain}/inventory/v1`
- **Official documentation:** [Get Item](https://www.zoho.com/inventory/api/v1/items/#retrieve-an-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `item_id` | path | `string` | yes | The Zoho Inventory item_id for the item. |
| `organization_id` | query | `string` | yes | Zoho Inventory organization ID to run this request against. |
