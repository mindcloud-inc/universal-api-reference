# Update Cart with Swell

## Endpoint

- **Method:** `PUT`
- **Path:** `/carts/:id`
- **Base URL:** `https://api.swell.store`
- **Official documentation:** [Update Cart](https://developers.swell.is/backend-api/carts/update-a-cart)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Swell cart ID. |
| `items[]` | body | `array<object>` | yes | Cart line items. |
| `billing` | body | `object` | no | Billing details. |
| `shipping` | body | `object` | no | Shipping details. |
| `coupon_code` | body | `string` | no | A coupon code to apply. |
