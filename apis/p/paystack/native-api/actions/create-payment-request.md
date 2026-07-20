# Create Payment Request with Paystack

## Endpoint

- **Method:** `POST`
- **Path:** `/paymentrequest`
- **Base URL:** `https://api.paystack.co`
- **Official documentation:** [Create Payment Request](https://paystack.com/docs/api/payment-request/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customer` | body | `string` | yes |
| `amount` | body | `number` | yes |
| `description` | body | `string` | yes |
| `due_date` | body | `string` | no |
