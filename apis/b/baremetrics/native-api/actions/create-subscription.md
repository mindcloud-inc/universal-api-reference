# Create Subscription with Baremetrics

Creates a subscription in Baremetrics.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/:source_id/subscriptions`
- **Base URL:** `https://sandbox.baremetrics.com`
- **Official documentation:** [Create Subscription](https://developers.baremetrics.com/reference/create-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_id` | path | `string` | yes | Please see [Sources](ref:sources) |
| `oid` | body | `string` | yes | Your unique ID for the subscription |
| `started_at` | body | `string` | yes | A unix timestamp of when this subscription started |
| `canceled_at` | body | `string` | no | A unix timestamp of when this subscription was, or should be canceled. This cannot be changed, so only set this if you are certain you know when the subscription will end. |
| `plan_oid` | body | `string` | yes | Your unique ID for the plan |
| `customer_oid` | body | `string` | yes | Your unique ID for the customer |
| `addons[]` | body | `array<object>` | no | — |
| `quantity` | body | `number` | no | — |
| `discount` | body | `number` | no | Integer value (in the same currency as the plan) |
