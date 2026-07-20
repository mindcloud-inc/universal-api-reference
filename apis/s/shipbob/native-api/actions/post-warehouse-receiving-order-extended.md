# Post Warehouse Receiving Order (Extended) with ShipBob

## Endpoint

- **Method:** `POST`
- **Path:** `2.0/receiving-extended`
- **Base URL:** `https://{apiSubdomain}.shipbob.com/`
- **API:** REST

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fulfillmentCenter.id` | body | `number` | no |
| `boxes[].boxItems[].quantity` | body | `string` | no |
| `boxes[].trackingNumber` | body | `string` | no |
| `fulfillment_center` | body | `object` | no |
| `tags[].name` | body | `string` | no |
| `boxes[].boxItems[]` | body | `array` | no |
| `boxes[].boxItems[].inventoryId` | body | `string` | no |
| `packageType` | body | `list` | no |
| `tags[].value` | body | `string` | no |
| `boxes[].boxItems[].lot_number` | body | `string` | no |
| `boxPackagingType` | body | `list` | no |
| `purchaseOrderNumber` | body | `string` | no |
| `expectedArrivalDate` | body | `string` | no |
| `boxes[]` | body | `array` | no |
| `fulfillmentCentere.id` | body | `string` | no |
| `fullasdfasdf.id` | body | `string` | no |
| `tags[]` | body | `array` | no |
