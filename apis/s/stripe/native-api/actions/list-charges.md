# List Charges with Stripe

## Endpoint

- **Method:** `GET`
- **Path:** `charges`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [List Charges](https://docs.stripe.com/api/charges/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customer` | query | `string` | no |
| `payment_intent` | query | `string` | no |
