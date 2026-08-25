# Get Payment Intent sync with Stripe

## Endpoint

- **Method:** `GET`
- **Path:** `payment_intents/:intent`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [Get Payment Intent sync](https://docs.stripe.com/api/payment_intents/retrieve)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `intent` | path | `string` | yes | PaymentIntent ID to retrieve (for example, pi_...). |
