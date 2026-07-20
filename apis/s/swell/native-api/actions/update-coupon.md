# Update Coupon with Swell

## Endpoint

- **Method:** `PUT`
- **Path:** `/coupons/:id`
- **Base URL:** `https://api.swell.store`
- **Official documentation:** [Update Coupon](https://developers.swell.is/backend-api/coupons/update-a-coupon)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Swell coupon ID. |
| `codes[]` | body | `array<object>` | no | Coupon code definitions. |
| `discounts[]` | body | `array<object>` | yes | Coupon discount rules. |
| `name` | body | `string` | no | The coupon name. |
| `active` | body | `boolean` | no | Whether the coupon is active. |
| `date_expired` | body | `date` | no | The coupon expiration timestamp. |
| `description` | body | `string` | no | The coupon description. |
| `multi_codes` | body | `boolean` | no | Whether the coupon supports multiple codes. |
