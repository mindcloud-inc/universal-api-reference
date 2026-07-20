# Mark Package As Shipped with TikTok Shop

This API is currently exclusive to the following markets: US, UK, ES, IE.

This API is for sellers who fulfill orders through their own selected/preferred logistics carrier, and allows sellers to upload valid package information (items in packages, shipping provider information, and tracking number) orders/order line items to TikTok Shop. Use Get Shipping Providers API to retrieve the shipping_provider_id for shipping providers.

## Endpoint

- **Method:** `POST`
- **Path:** `fulfillment/202309/orders/:order_id/packages`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [Mark Package As Shipped](https://partner.tiktokshop.com/docv2/page/mark-package-as-shipped)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `order_id` | path | `string` | yes |
| `shipping_provider_id` | body | `string` | yes |
| `shop_cipher` | query | `list<string>` | yes |
| `tracking_number` | body | `string` | no |
| `order_line_item_ids[]` | body | `array<string>` | no |
