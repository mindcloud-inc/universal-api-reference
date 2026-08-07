# Post Warehouse Receiving Order with ShipBob

## Endpoint

- **Method:** `POST`
- **Path:** `2026-07/receiving`
- **Base URL:** `https://{apiSubdomain}.shipbob.com/`
- **API:** REST
- **Official documentation:** [Post Warehouse Receiving Order](https://developer.shipbob.com/api/receiving/create-warehouse-receiving-order)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `boxes[].boxItems[].quantity` | body | `string` | no |
| `boxes[].trackingNumber` | body | `string` | no |
| `fulfillment_center.id` | body | `number` | no |
| `packageType` | body | `list` | no |
| `boxes[].boxItems[]` | body | `array` | no |
| `boxes[].boxItems[].inventoryId` | body | `string` | no |
| `boxPackagingType` | body | `list` | no |
| `boxes[].boxItems[].lot_number` | body | `string` | no |
| `purchaseOrderNumber` | body | `string` | no |
| `expectedArrivalDate` | body | `string` | no |
| `boxes[]` | body | `array` | no |
| `final_destination_fulfillment_center_id` | body | `number` | no |
| `fulfillment_center` | body | `object` | no |
| `fulfillmentCentere.id` | body | `string` | no |
| `fullasdfasdf.id` | body | `string` | no |
