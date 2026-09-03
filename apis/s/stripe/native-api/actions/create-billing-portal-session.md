# Create Billing Portal Session with Stripe

## Endpoint

- **Method:** `POST`
- **Path:** `billing_portal/sessions`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [Create Billing Portal Session](https://docs.stripe.com/api/customer_portal/sessions/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customer` | body | `string` | yes |
| `return_url` | body | `string` | no |
| `configuration` | body | `string` | no |
