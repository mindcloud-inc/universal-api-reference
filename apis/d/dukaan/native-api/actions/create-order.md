# Create Order with Dukaan

Creates a new order in Dukaan.

## Endpoint

- **Method:** `POST`
- **Path:** `api/order/seller/order/`
- **Base URL:** `https://api.mydukaan.io`
- **Official documentation:** [Create Order](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `store` | body | `string` | yes | Store UUID for the order. |
| `line_items[]` | body | `array<object>` | yes | Order line item objects. |
| `mobile` | body | `string` | yes | Buyer mobile number. |
| `buyer_pin` | body | `string` | no | Buyer postal code. |
| `address` | body | `object` | yes | Buyer address object. |
| `notes` | body | `string` | no | Order notes. |
| `payment_mode` | body | `number` | no | Dukaan payment mode code. |
