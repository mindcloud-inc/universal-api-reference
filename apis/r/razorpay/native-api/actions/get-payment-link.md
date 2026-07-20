# Get Payment Link with Razorpay

Retrieves a payment link from Razorpay by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/payment_links/:id`
- **Base URL:** `https://api.razorpay.com`
- **Official documentation:** [Get Payment Link](https://razorpay.com/docs/api/payments/payment-links/fetch-id-standard/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the payment link. |
