# Mark Shipment Order Delivered with Zoho Inventory

Marks a shipment order as delivered in Zoho Inventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/shipmentorders/:shipmentorder_id/status/delivered`
- **Base URL:** `{api_domain}/inventory/v1`
- **Official documentation:** [Mark Shipment Order Delivered](https://www.zoho.com/inventory/api/v1/shipmentorders/#mark-as-delivered)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shipmentorder_id` | path | `string` | yes | The Zoho Inventory shipmentorder_id for the shipment order. |
| `organization_id` | query | `string` | yes | Zoho Inventory organization ID to run this request against. |
