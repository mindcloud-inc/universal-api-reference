# Ship Package with TikTok Shop

Use this API to ship a package. There are two kinds of shipping options available: TikTok Shipping or Seller Shipping.

- TikTok Shipping: Schedule a package handover time for TikTok Shipping carriers to pickup a package from seller.
- Seller Shipping: Seller arranges their own shipping, and uploads a tracking number and shipping_provider_id. Package ID can be obtained from Get Order Detail

## Endpoint

- **Method:** `POST`
- **Path:** `fulfillment/202309/packages/:package_id/ship`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [Ship Package](https://partner.tiktokshop.com/docv2/page/ship-package-202309)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `package_id` | path | `string` | yes | — |
| `pickupSlot.startTime` | body | `number` | no | The start date and time of the package pickup time slot. Unix timestamp. |
| `selfShipment.trackingNumber` | body | `string` | no | For package with SEND_BY_SELLER as delivery_option (merchant self-shipping mode), you must input a tracking_number to call this API. |
| `handoverMethod` | body | `string` | no | Possible values: - PICKUP: A logistics carrier will pick up the package(s) from the seller's pickup address. - DROP_OFF: The seller will need to drop off the package(s) to a designated location. |
| `pickupSlot.endTime` | body | `number` | no | The end date and time of the package pickup time slot. Unix timestamp. |
| `selfShipment.shippingProviderid` | body | `string` | no | For package with SEND_BY_SELLER as delivery_option (merchant self-shipping mode), you must input a shipping_provider_id to call this API. Please use Get Shipping Providers to obtain the shipping_provider_id. |
| `pickupSlot` | body | `object` | no | Pickup time slot. |
| `selfShipment` | body | `object` | no | Only needed for merchant self-shipping packages. Check the delivery_option field of Get Package Detail to see how to differentiate platform-logistics and self-shipping. Use the shipping_provider_id retrieved from Get Shipping Providers and upload the corresponding tracking_number. |
| `shop_cipher` | query | `list<string>` | yes | — |
