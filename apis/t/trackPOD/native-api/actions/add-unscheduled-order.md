# Add Unscheduled Order with Track-POD

Creates a new unscheduled order in Track-POD.

## Endpoint

- **Method:** `POST`
- **Path:** `/Order`
- **Base URL:** `https://api.track-pod.com`
- **Official documentation:** [Add Unscheduled Order](https://api.track-pod.com/index.html#/Order/AddOrder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Address` | body | `string` | no | Delivery address. |
| `AddressLat` | body | `number` | no | Delivery latitude. |
| `AddressLon` | body | `number` | no | Delivery longitude. |
| `AddressZone` | body | `string` | no | Delivery address zone. |
| `Barcode` | body | `string` | no | Order barcode. |
| `Client` | body | `string` | no | Client name. |
| `COD` | body | `number` | no | Cash on delivery amount. |
| `ContactName` | body | `string` | no | Recipient contact name. |
| `CustomerReferenceId` | body | `string` | no | Customer reference identifier. |
| `CustomFields[0].Id` | body | `string` | no | First custom field identifier. |
| `CustomFields[0].Value` | body | `string` | no | First custom field value. |
| `CustomFields[1].Id` | body | `string` | no | Second custom field identifier. |
| `CustomFields[1].Value` | body | `string` | no | Second custom field value. |
| `Date` | body | `string` | no | Order date and time. |
| `Depot` | body | `string` | no | Depot name. |
| `Email` | body | `string` | no | Recipient email. |
| `GoodsList[0].Cost` | body | `number` | no | First goods cost. |
| `GoodsList[0].GoodsBarcode` | body | `string` | no | First goods barcode. |
| `GoodsList[0].GoodsId` | body | `string` | no | First goods item identifier. |
| `GoodsList[0].GoodsName` | body | `string` | no | First goods item name. |
| `GoodsList[0].GoodsUnit` | body | `string` | no | First goods unit. |
| `GoodsList[0].Note` | body | `string` | no | First goods note. |
| `GoodsList[0].OrderLineBarcode` | body | `string` | no | First goods order-line barcode. |
| `GoodsList[0].OrderLineId` | body | `string` | no | First goods line identifier. |
| `GoodsList[0].Quantity` | body | `number` | no | First goods quantity. |
| `GoodsList[1].Cost` | body | `number` | no | Second goods cost. |
| `GoodsList[1].GoodsBarcode` | body | `string` | no | Second goods barcode. |
| `GoodsList[1].GoodsId` | body | `string` | no | Second goods item identifier. |
| `GoodsList[1].GoodsName` | body | `string` | no | Second goods item name. |
| `GoodsList[1].GoodsUnit` | body | `string` | no | Second goods unit. |
| `GoodsList[1].Note` | body | `string` | no | Second goods note. |
| `GoodsList[1].OrderLineBarcode` | body | `string` | no | Second goods order-line barcode. |
| `GoodsList[1].OrderLineId` | body | `string` | no | Second goods line identifier. |
| `GoodsList[1].Quantity` | body | `number` | no | Second goods quantity. |
| `Id` | body | `string` | no | Order identifier. |
| `InvoiceId` | body | `string` | no | Invoice identifier. |
| `Note` | body | `string` | no | Order note. |
| `NotificationsPolicy.AtDepartureNotificationEnabled` | body | `boolean` | no | Send a departure notification. |
| `NotificationsPolicy.AtRouteStartNotificationEnabled` | body | `boolean` | no | Send a route-start notification. |
| `NotificationsPolicy.EnRouteNotificationEnabled` | body | `boolean` | no | Send an en-route notification. |
| `NotificationsPolicy.PriorToRouteNotificationEnabled` | body | `boolean` | no | Send a prior-to-route notification. |
| `Number` | body | `string` | no | Order number. |
| `Pallets` | body | `number` | no | Order pallets. |
| `Phone` | body | `string` | no | Recipient phone number. |
| `PickupOrder.Address` | body | `string` | no | Pickup address. |
| `PickupOrder.AddressId` | body | `string` | no | Pickup address identifier. |
| `PickupOrder.AddressLat` | body | `number` | no | Pickup latitude. |
| `PickupOrder.AddressLon` | body | `number` | no | Pickup longitude. |
| `PickupOrder.AddressZone` | body | `string` | no | Pickup address zone. |
| `PickupOrder.Client` | body | `string` | no | Pickup client name. |
| `PickupOrder.ClientId` | body | `string` | no | Pickup client identifier. |
| `PickupOrder.COD` | body | `number` | no | Pickup cash on delivery amount. |
| `PickupOrder.ContactName` | body | `string` | no | Pickup contact name. |
| `PickupOrder.CustomFields[0].Id` | body | `string` | no | First pickup custom field identifier. |
| `PickupOrder.CustomFields[0].Value` | body | `string` | no | First pickup custom field value. |
| `PickupOrder.CustomFields[1].Id` | body | `string` | no | Second pickup custom field identifier. |
| `PickupOrder.CustomFields[1].Value` | body | `string` | no | Second pickup custom field value. |
| `PickupOrder.Email` | body | `string` | no | Pickup email. |
| `PickupOrder.Note` | body | `string` | no | Pickup note. |
| `PickupOrder.Phone` | body | `string` | no | Pickup phone number. |
| `PickupOrder.ServiceTime` | body | `number` | no | Pickup service time. |
| `PickupOrder.TimeSlotFrom` | body | `string` | no | Pickup time window start. |
| `PickupOrder.TimeSlotTo` | body | `string` | no | Pickup time window end. |
| `Priority` | body | `number` | no | Order priority. |
| `ServiceTime` | body | `number` | no | Planned service time. |
| `Shipper` | body | `string` | no | Shipper name. |
| `TeamCode` | body | `string` | no | Team code. |
| `TimeSlotFrom` | body | `string` | no | Start of the delivery time window. |
| `TimeSlotTo` | body | `string` | no | End of the delivery time window. |
| `Type` | body | `number` | no | Order type. |
| `updateAddressGps` | query | `boolean` | no | Force-update existing address latitude/longitude from the payload. |
| `updateGoodsPrice` | query | `boolean` | no | Force-update existing goods prices from the payload. |
| `Volume` | body | `number` | no | Order volume. |
| `Weight` | body | `number` | no | Order weight. |
