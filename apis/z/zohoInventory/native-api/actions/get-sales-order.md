# Get Sales Order with Zoho Inventory

Retrieves a sales order from Zoho Inventory.

## Endpoint

- **Method:** `GET`
- **Path:** `/salesorders/:salesorder_id`
- **Base URL:** `{api_domain}/inventory/v1`
- **Official documentation:** [Get Sales Order](https://www.zoho.com/inventory/api/v1/salesorders/#retrieve-a-sales-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `salesorder_id` | path | `string` | yes | The Zoho Inventory salesorder_id for the sales order. |
| `organization_id` | query | `string` | yes | Zoho Inventory organization ID to run this request against. |
