# List Subscriptions with Stripe

## Endpoint

- **Method:** `GET`
- **Path:** `subscriptions`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [List Subscriptions](https://docs.stripe.com/api/subscriptions/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer` | query | `string` | no | Only return subscriptions for this Stripe customer ID. |
| `status` | query | `list<string>` | no | Only return subscriptions with the selected Stripe subscription status. Accepted values: `active`, `all`, `canceled`, `ended`, `incomplete`, `incomplete_expired`, `past_due`, `paused`, `trialing`, `unpaid`. |
| `collection_method` | query | `list<string>` | no | Only return subscriptions collected automatically or paid by sent invoice. Accepted values: `charge_automatically`, `send_invoice`. |
| `price` | query | `string` | no | Only return subscriptions containing this recurring Stripe price ID. |
