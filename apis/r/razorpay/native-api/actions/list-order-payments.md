# List Order Payments with Razorpay

Retrieves payments for a specific order from Razorpay.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/orders/:id/payments`
- **Base URL:** `https://api.razorpay.com`
- **Official documentation:** [List Order Payments](https://razorpay.com/docs/api/orders/fetch-payments/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the order. |
