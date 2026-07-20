# Expire Checkout Session with Stripe

Expires an existing checkout session in Stripe.

## Endpoint

- **Method:** `POST`
- **Path:** `checkout/sessions/:session/expire`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [Expire Checkout Session](https://docs.stripe.com/api/checkout/sessions/expire)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `session` | path | `string` | yes | Checkout session ID to expire. |
