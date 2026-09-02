# Create Payment Intent with Stripe

Creates a new payment intent in Stripe.

## Endpoint

- **Method:** `POST`
- **Path:** `payment_intents`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [Create Payment Intent](https://docs.stripe.com/api/payment_intents/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | yes | Amount intended to be collected, in the smallest currency unit. |
| `currency` | body | `string` | yes | Three-letter ISO currency code, in lowercase. |
| `customer` | body | `string` | no | Customer ID to attach to the PaymentIntent. |
| `payment_method` | body | `string` | no | PaymentMethod ID to attach to this PaymentIntent. |
| `description` | body | `string` | no | An arbitrary string attached to the object. |
| `confirm` | body | `boolean` | no | Set to true to attempt to confirm this PaymentIntent immediately. |
| `capture_method` | body | `list<string>` | no | Controls when funds are captured from the customer. Accepted values: `automatic`, `automatic_async`, `manual`. |
| `metadata` | body | `object` | no | — |
| `off_session` | body | `boolean` | no | — |
| `idempotencyKey` | body | `string` | no | — |
