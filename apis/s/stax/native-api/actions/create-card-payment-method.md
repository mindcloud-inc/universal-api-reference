# Create Card Payment Method with Stax

Creates a card payment method in Stax.

## Endpoint

- **Method:** `POST`
- **Path:** `/payment-method/`
- **Base URL:** `https://apiprod.fattlabs.com`
- **Official documentation:** [Create Card Payment Method](https://docs.staxpayments.com/reference/create-a-payment-method)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address_zip` | body | `string` | no | Billing zip code |
| `card_exp` | body | `string` | no | Card expiration |
| `card_number` | body | `string` | no | Card number |
| `customer_id` | body | `string` | no | Customer identifier |
| `method` | body | `string` | no | Payment method type |
| `person_name` | body | `string` | no | Cardholder name |
