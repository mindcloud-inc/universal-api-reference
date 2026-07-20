# Cancel Payment Intent with Stripe

Cancels an existing payment intent in Stripe.

## Endpoint

- **Method:** `POST`
- **Path:** `payment_intents/:intent/cancel`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [Cancel Payment Intent](https://docs.stripe.com/api/payment_intents/cancel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `intent` | path | `string` | yes | PaymentIntent ID to cancel. |
| `cancellation_reason` | body | `list<string>` | no | Reason for cancellation. Accepted values: `abandoned`, `duplicate`, `fraudulent`, `requested_by_customer`. |
