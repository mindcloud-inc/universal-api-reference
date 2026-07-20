# Confirm Sales Order with Zoho Inventory

Marks a sales order as confirmed in Zoho Inventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/salesorders/:salesorder_id/status/confirmed`
- **Base URL:** `{api_domain}/inventory/v1`
- **Official documentation:** [Confirm Sales Order](https://www.zoho.com/inventory/api/v1/salesorders/#mark-as-confirmed)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `salesorder_id` | path | `string` | yes | The Zoho Inventory salesorder_id for the sales order. |
| `organization_id` | query | `string` | yes | Zoho Inventory organization ID to run this request against. |
