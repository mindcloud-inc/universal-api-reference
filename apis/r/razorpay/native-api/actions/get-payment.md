# Get Payment with Razorpay

Retrieves a payment from Razorpay by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/payments/:id`
- **Base URL:** `https://api.razorpay.com`
- **Official documentation:** [Get Payment](https://razorpay.com/docs/api/payments/fetch-with-id/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the payment. |
