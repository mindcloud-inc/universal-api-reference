# List Subscription Schedules with Stripe

## Endpoint

- **Method:** `GET`
- **Path:** `subscription_schedules`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [List Subscription Schedules](https://docs.stripe.com/api/subscription_schedules/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customer` | query | `string` | no |
| `scheduled` | query | `boolean` | no |
