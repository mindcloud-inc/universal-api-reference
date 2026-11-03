# Ship Order with Rithum for Brands

Mark an entire order as shipped or partially shipped.

## Endpoint

- **Method:** `POST`
- **Path:** `Orders(:orderId)/Ship`
- **Base URL:** `https://api.channeladvisor.com/v1/`
- **Official documentation:** [Ship Order](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_kb_id=b20d13092fd15994cffb5ff62799b602)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Items[].OrderItemID` | body | `string` | no | When the Items array is included in this request, one of: OrderItemID or ProductID or Sku is required. |
| `orderId` | path | `string` | no | — |
| `ShippedDateUtc` | body | `string` | no | — |
| `Items[].ProductID` | body | `string` | no | Identifies the item by Product ID. (conditionally required) |
| `TrackingNumber` | body | `string` | no | — |
| `Items[].Sku` | body | `string` | no | (conditionally required) Identifies the SKU (as defined by the seller). |
| `ReturnTrackingNumber` | body | `string` | no | — |
| `Items[].Quantity` | body | `string` | no | Required if the Items array is included in this request. |
| `ShippingCarrier` | body | `string` | no | — |
| `Items[].SellerFulfillmentItemID` | body | `string` | no | (optional) Identifier provided by the seller. Usually a serial number or batch number. |
| `ShippingClass` | body | `string` | no | — |
| `DeliveryStatus` | body | `string` | no | Complete is the most common status used. See all here: https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_id=c568b05533206e10ae51a5373e5c7b0e&spa=1#concept-89__section-3115 |
| `TrackingUrl` | body | `string` | no | — |
| `DistributionCenterID` | body | `number` | no | — |
| `Items[]` | body | `array<object>` | no | (optional) A list of items to mark as shipped for this order. Leaving this array empty will mark the entire order as shipped. |
