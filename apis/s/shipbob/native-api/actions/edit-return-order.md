# Edit Return Order with ShipBob

## Endpoint

- **Method:** `PUT`
- **Path:** `2026-07/return/:id`
- **Base URL:** `https://{apiSubdomain}.shipbob.com/`
- **API:** REST
- **Official documentation:** [Edit Return Order](https://developer.shipbob.com/api/returns/edit-return-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ShipBob return order ID to edit. |
| `fulfillment_center` | body | `object` | yes | The fulfillment center receiving the return. |
| `fulfillment_center.id` | body | `list<number>` | yes | The ShipBob fulfillment center that will receive the return. |
| `inventory[]` | body | `array<object>` | yes | The returned inventory items and requested handling actions. |
| `inventory[].id` | body | `list<number>` | yes | The ShipBob inventory item being returned. |
| `inventory[].quantity` | body | `number` | yes | The quantity of this inventory item being returned. |
| `inventory[].requested_action` | body | `list` | yes | How ShipBob should handle this returned inventory item. Accepted values: `0`, `1`, `2`, `3`. |
| `inventory[].lot_date` | body | `date` | no | The lot date for this inventory item, when applicable. |
| `inventory[].lot_number` | body | `string` | no | The lot number for this inventory item, when applicable. |
| `reference_id` | body | `string` | yes | Your unique reference for this return order. Maximum length: 50. |
| `original_shipment_id` | body | `number` | no | The original ShipBob shipment ID, when available. |
| `tracking_number` | body | `string` | no | The carrier tracking number for the return package. Maximum length: 500. |
