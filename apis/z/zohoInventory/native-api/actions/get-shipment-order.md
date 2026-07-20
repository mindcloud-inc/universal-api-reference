# Get Shipment Order with Zoho Inventory

Retrieves a shipment order from Zoho Inventory.

## Endpoint

- **Method:** `GET`
- **Path:** `/shipmentorders/:shipmentorder_id`
- **Base URL:** `{api_domain}/inventory/v1`
- **Official documentation:** [Get Shipment Order](https://www.zoho.com/inventory/api/v1/shipmentorders/#retrieve-a-shipment-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shipmentorder_id` | path | `string` | yes | The Zoho Inventory shipmentorder_id for the shipment order. |
| `organization_id` | query | `string` | yes | Zoho Inventory organization ID to run this request against. |
