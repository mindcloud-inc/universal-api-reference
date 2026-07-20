# Create Charge with Poof

Creates a new fiat charge in Poof.

## Endpoint

- **Method:** `POST`
- **Path:** `https://www.poof.io/api/v1/create_fiat_charge`
- **Base URL:** `https://www.poof.io/api/v2`
- **Official documentation:** [Create Charge](https://docs.poof.io/reference/createcharge)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `string` | yes | Charge amount. |
| `payment` | body | `string` | yes | Fiat payment method; docs example uses paypal. |
| `currency` | body | `string` | yes | Fiat currency code. |
| `redirect_url` | body | `string` | yes | Redirect URL. |
| `success_url` | body | `string` | yes | Success URL. |
