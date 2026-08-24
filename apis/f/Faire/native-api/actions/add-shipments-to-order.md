# Add Shipments to Order with Faire

## Endpoint

- **Method:** `POST`
- **Path:** `orders/:orderId/shipments`
- **Base URL:** `https://www.faire.com/external-api/v2/`
- **Official documentation:** [Add Shipments to Order](https://developers.faire.com/docs#/paths/orders-order_id--shipments/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | The ID of the order to add shipments to. |
| `shipments[]` | body | `array<object>` | no | A list of shipments to add to the order. Send multiple values as a array. |
| `shipments[].order_id` | body | `string` | no | The ID of the order the shipment is attached to. |
| `shipments[].carrier` | body | `string` | no | The carrier used to ship the order. Accepted values are case insensitive; Faire may also attempt to recognize other carrier names. Carriers: CANADA_POST, DHL_ECOMMERCE, DHL_EXPRESS, FEDEX, PUROLATOR, UPS, USPS, POSTNL, CANPAR, INTERLINK_EXPRESS, GSO, ROYAL_MAIL, DPD, DPDUK, PARCELFORCE, AUSTRALIA_POST, EVRI, and LA_POSTE |
| `shipments[].tracking_code` | body | `string` | no | The tracking code for the shipment; its format varies by carrier. |
| `shipments[].maker_cost` | body | `object` | no | The cost the brand paid to ship the order. |
| `shipments[].maker_cost.amount_minor` | body | `number` | no | The amount in the smallest unit of the currency, such as cents for USD. |
| `shipments[].makerCost.currency` | body | `string` | no | The currency in ISO 4217 format, such as USD. |
| `shipments[].shipping_type` | body | `list<string>` | no | How the shipment is handled: the brand ships it or uses Faire's shipping service. Accepted values: `SHIP_ON_YOUR_OWN`, `SHIP_WITH_FAIRE`. |
