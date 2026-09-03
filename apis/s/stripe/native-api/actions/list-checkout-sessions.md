# List Checkout Sessions with Stripe

## Endpoint

- **Method:** `GET`
- **Path:** `checkout/sessions`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [List Checkout Sessions](https://docs.stripe.com/api/checkout/sessions/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer` | query | `string` | no | — |
| `status` | query | `list` | no | Accepted values: `0`, `1`, `2`. |
| `payment_intent` | query | `string` | no | — |
| `subscription` | query | `string` | no | — |
| `payment_link` | query | `string` | no | — |
