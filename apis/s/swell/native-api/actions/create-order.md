# Create Order with Swell

## Endpoint

- **Method:** `POST`
- **Path:** `/orders`
- **Base URL:** `https://api.swell.store`
- **Official documentation:** [Create Order](https://developers.swell.is/backend-api/orders/create-an-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | body | `string` | no | The Swell account ID. |
| `items[]` | body | `array<object>` | yes | Order line items. |
| `billing` | body | `object` | no | Billing details. |
| `shipping` | body | `object` | no | Shipping details. |
| `coupon_code` | body | `string` | no | A coupon code to apply. |
