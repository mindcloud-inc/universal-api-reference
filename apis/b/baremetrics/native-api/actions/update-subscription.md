# Update Subscription with Baremetrics

Updates a subscription in Baremetrics.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/:source_id/subscriptions/:subscription_oid`
- **Base URL:** `https://sandbox.baremetrics.com`
- **Official documentation:** [Update Subscription](https://developers.baremetrics.com/reference/update-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscription_oid` | path | `string` | yes | Your unique ID for the subscription |
| `source_id` | path | `string` | yes | Please see [Sources](ref:sources) |
| `plan_oid` | body | `string` | yes | Your unique ID for the plan |
| `occurred_at` | body | `string` | no | A unix timestamp of when this change occurred. Defaults to now |
| `addons[]` | body | `array<object>` | no | In cents. The OID can be anything you want. |
| `quantity` | body | `number` | no | — |
| `discount` | body | `number` | no | Integer value (in the same currency as the plan) |
