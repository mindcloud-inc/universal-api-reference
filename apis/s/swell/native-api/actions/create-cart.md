# Create Cart with Swell

## Endpoint

- **Method:** `POST`
- **Path:** `/carts`
- **Base URL:** `https://api.swell.store`
- **Official documentation:** [Create Cart](https://developers.swell.is/backend-api/carts/create-a-cart)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `items[]` | body | `array<object>` | yes | Cart line items. |
| `billing` | body | `object` | no | Billing details. |
| `shipping` | body | `object` | no | Shipping details. |
| `coupon_code` | body | `string` | no | A coupon code to apply. |
