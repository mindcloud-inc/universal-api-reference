# List Payment Intents with Stripe

Retrieves payment intents from your Stripe account.

## Endpoint

- **Method:** `GET`
- **Path:** `payment_intents`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [List Payment Intents](https://docs.stripe.com/api/payment_intents/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | — |
| `customer` | query | `string` | no | Only return PaymentIntents for this customer ID. |
| `starting_after` | query | `string` | no | — |
| `ending_before` | query | `string` | no | — |
| `created` | query | `object` | no | Filter by creation timestamp or range object. |
| `customer_account` | query | `string` | no | — |
| `expand[]` | query | `array<string>` | no | — |
