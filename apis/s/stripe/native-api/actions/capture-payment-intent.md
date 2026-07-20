# Capture Payment Intent with Stripe

Captures an existing payment intent in Stripe.

## Endpoint

- **Method:** `POST`
- **Path:** `payment_intents/:intent/capture`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [Capture Payment Intent](https://docs.stripe.com/api/payment_intents/capture)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `intent` | path | `string` | yes | PaymentIntent ID to capture. |
| `amount_to_capture` | body | `number` | no | Amount to capture from the PaymentIntent. |
| `final_capture` | body | `boolean` | no | Set to false when performing incremental captures. |
