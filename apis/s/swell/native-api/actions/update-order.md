# Update Order with Swell

## Endpoint

- **Method:** `PUT`
- **Path:** `/orders/:id`
- **Base URL:** `https://api.swell.store`
- **Official documentation:** [Update Order](https://developers.swell.is/backend-api/orders/update-an-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Swell order ID. |
| `account_id` | body | `string` | no | The Swell account ID. |
| `items[]` | body | `array<object>` | yes | Order line items. |
| `billing` | body | `object` | no | Billing details. |
| `shipping` | body | `object` | no | Shipping details. |
| `coupon_code` | body | `string` | no | A coupon code to apply. |
