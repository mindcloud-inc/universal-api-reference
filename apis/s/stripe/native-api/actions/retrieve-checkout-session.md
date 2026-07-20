# Retrieve Checkout Session with Stripe

Retrieves a checkout session from Stripe.

## Endpoint

- **Method:** `GET`
- **Path:** `checkout/sessions/:session`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [Retrieve Checkout Session](https://docs.stripe.com/api/checkout/sessions/retrieve)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `session` | path | `string` | yes | Checkout session ID to retrieve. |
