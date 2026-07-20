# Create Payment Refund with Razorpay

Creates a refund for a payment in Razorpay.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/payments/:id/refund`
- **Base URL:** `https://api.razorpay.com`
- **Official documentation:** [Create Payment Refund](https://razorpay.com/docs/api/refunds/create-normal/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the payment. |
| `amount` | body | `number` | no | — |
| `speed` | body | `string` | no | — |
| `notes` | body | `object` | no | — |
| `receipt` | body | `string` | no | — |
