# Update Payment Link with Razorpay

Updates an existing payment link in Razorpay.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/payment_links/:id`
- **Base URL:** `https://api.razorpay.com`
- **Official documentation:** [Update Payment Link](https://razorpay.com/docs/api/payments/payment-links/update-standard/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the payment link. |
| `accept_partial` | body | `boolean` | no | — |
| `reference_id` | body | `string` | no | — |
| `expire_by` | body | `number` | no | — |
| `notes` | body | `object` | no | — |
