# Update Payment Method with Stax

Updates a payment method in Stax.

## Endpoint

- **Method:** `PUT`
- **Path:** `/payment-method/:id`
- **Base URL:** `https://apiprod.fattlabs.com`
- **Official documentation:** [Update Payment Method](https://docs.staxpayments.com/reference/update-a-payment-method)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address_zip` | body | `string` | no | Billing zip code |
| `id` | path | `string` | no | Payment method identifier |
| `person_name` | body | `string` | no | Cardholder or account holder name |
