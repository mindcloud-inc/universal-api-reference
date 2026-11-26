# Create Return Order with ShipBob

## Endpoint

- **Method:** `POST`
- **Path:** `2026-07/return`
- **Base URL:** `https://{apiSubdomain}.shipbob.com/`
- **API:** REST
- **Official documentation:** [Create Return Order](https://developer.shipbob.com/api/returns/create-return-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fulfillment_center` | body | `object` | yes | The fulfillment center that will process the return. |
| `fulfillment_center.id` | body | `list<number>` | yes | The ShipBob fulfillment center ID. |
| `inventory[]` | body | `array<object>` | yes | The physical inventory items included in this return. |
| `inventory[].id` | body | `list<number>` | yes | The ShipBob inventory item ID. |
| `inventory[].quantity` | body | `number` | yes | The quantity of this inventory item being returned. |
| `inventory[].requested_action` | body | `list<string>` | yes | How ShipBob should handle the returned item: Default, Restock, Quarantine, or Dispose. Accepted values: `Default`, `Dispose`, `Quarantine`, `Restock`. |
| `inventory[].lot_date` | body | `date` | no | The lot date for a lot-tracked inventory item. |
| `inventory[].lot_number` | body | `string` | no | The lot number for a lot-tracked inventory item. |
| `reference_id` | body | `string` | yes | A unique external reference or RMA number for this return. Maximum length: 50. |
| `original_shipment_id` | body | `number` | no | The shipment from which the returned items originated. |
| `tracking_number` | body | `string` | no | The tracking number for the return shipment. Maximum length: 500. |
