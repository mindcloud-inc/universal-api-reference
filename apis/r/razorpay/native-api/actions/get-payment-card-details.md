# Get Payment Card Details with Razorpay

Retrieves card details for a payment from Razorpay.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/payments/:id/card`
- **Base URL:** `https://api.razorpay.com`
- **Official documentation:** [Get Payment Card Details](https://razorpay.com/docs/api/payments/fetch-card-details-payment/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the payment. |
