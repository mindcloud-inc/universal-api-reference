# List Payment Refunds with Razorpay

Retrieves refunds for a specific payment from Razorpay.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/payments/:id/refunds`
- **Base URL:** `https://api.razorpay.com`
- **Official documentation:** [List Payment Refunds](https://razorpay.com/docs/api/refunds/fetch-multiple-refund-payment/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the payment. |
