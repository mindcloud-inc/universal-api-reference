# Update Shipment with Cratejoy

Updates an existing shipment in Cratejoy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/shipments/:shipId/`
- **Base URL:** `https://api.cratejoy.com`
- **Official documentation:** [Update Shipment](https://docs.cratejoy.com/reference/shipment-methods-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shipId` | path | `number` | yes | The Cratejoy shipment ID. |
| `adjusted_ordered_at` | body | `string` | no | The target ship date for the shipment. |
| `tracking_number` | body | `string` | no | The tracking number for the shipment. |
| `status` | body | `string` | no | The shipment status. |
| `carrier_name` | body | `string` | no | The shipment carrier name. |
| `tracking_link` | body | `string` | no | The tracking URL for the shipment. |
| `shipped_at` | body | `string` | no | The shipped timestamp for the shipment. |
