# List Refunds with Stripe

## Endpoint

- **Method:** `GET`
- **Path:** `refunds`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [List Refunds](https://docs.stripe.com/api/refunds/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `charge` | query | `string` | no |
| `payment_intent` | query | `string` | no |
