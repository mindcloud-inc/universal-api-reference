# Capture Payment with Razorpay

Captures an authorized payment in Razorpay.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/payments/:id/capture`
- **Base URL:** `https://api.razorpay.com`
- **Official documentation:** [Capture Payment](https://razorpay.com/docs/api/payments/capture/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the payment. |
| `amount` | body | `number` | yes | Amount to capture in the smallest currency subunit. |
| `currency` | body | `string` | yes | ISO currency code for capture (for example INR). |
