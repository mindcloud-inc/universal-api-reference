# Confirm Payment Intent with Stripe

Confirms an existing payment intent in Stripe.

## Endpoint

- **Method:** `POST`
- **Path:** `payment_intents/:intent/confirm`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [Confirm Payment Intent](https://docs.stripe.com/api/payment_intents/confirm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `intent` | path | `string` | yes | PaymentIntent ID to confirm. |
| `payment_method` | body | `string` | no | PaymentMethod ID to use for confirmation. |
| `receipt_email` | body | `string` | no | Email that receives the payment receipt. |
| `return_url` | body | `string` | no | Return URL for redirect-based payment methods. |
| `off_session` | body | `boolean` | no | Set to true when charging a customer who is not in-session. |
