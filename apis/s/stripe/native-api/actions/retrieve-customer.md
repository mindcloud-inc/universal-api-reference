# Retrieve Customer with Stripe

Retrieves a customer from your Stripe account.

## Endpoint

- **Method:** `GET`
- **Path:** `customers/:customer`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [Retrieve Customer](https://docs.stripe.com/api/customers/retrieve)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customer` | path | `string` | yes |
| `expand[]` | query | `array<string>` | no |
