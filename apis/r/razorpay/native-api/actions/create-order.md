# Create Order with Razorpay

Creates a new order in Razorpay.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/orders`
- **Base URL:** `https://api.razorpay.com`
- **Official documentation:** [Create Order](https://razorpay.com/docs/api/orders/create/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | yes | Order amount in the smallest currency subunit. |
| `currency` | body | `string` | yes | ISO currency code (for example INR). |
| `receipt` | body | `string` | no | — |
| `notes` | body | `object` | no | — |
