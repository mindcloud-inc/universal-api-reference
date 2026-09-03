# List Events with Stripe

## Endpoint

- **Method:** `GET`
- **Path:** `events`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [List Events](https://docs.stripe.com/api/events/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `type` | query | `string` | no |
| `delivery_success` | query | `boolean` | no |
