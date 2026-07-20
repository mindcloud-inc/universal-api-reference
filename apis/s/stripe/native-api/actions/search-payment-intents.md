# Search Payment Intents with Stripe

Finds payment intents in Stripe by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `payment_intents/search`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [Search Payment Intents](https://docs.stripe.com/api/payment_intents/search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | The query argument that is going to be passed onto the Stripe Api |
| `limit` | query | `number` | no | — |
| `page` | query | `string` | no | — |
| `expand[]` | query | `array<string>` | no | — |
