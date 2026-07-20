# Create Payment Link with Razorpay

Creates a new payment link in Razorpay.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/payment_links`
- **Base URL:** `https://api.razorpay.com`
- **Official documentation:** [Create Payment Link](https://razorpay.com/docs/api/payments/payment-links/create-standard/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | yes | Payment link amount in the smallest currency subunit. |
| `currency` | body | `string` | no | ISO currency code (for example INR). |
| `accept_partial` | body | `boolean` | no | — |
| `first_min_partial_amount` | body | `number` | no | — |
| `upi_link` | body | `boolean` | no | — |
| `description` | body | `string` | no | — |
| `reference_id` | body | `string` | no | — |
| `customer` | body | `object` | no | — |
| `notify` | body | `object` | no | — |
| `expire_by` | body | `number` | no | — |
| `notes` | body | `object` | no | — |
| `callback_url` | body | `string` | no | — |
| `callback_method` | body | `string` | no | — |
| `reminder_enable` | body | `boolean` | no | — |
