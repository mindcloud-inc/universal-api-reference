# List Disputes with Stripe

## Endpoint

- **Method:** `GET`
- **Path:** `disputes`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [List Disputes](https://docs.stripe.com/api/disputes/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `charge` | query | `string` | no |
| `payment_intent` | query | `string` | no |
