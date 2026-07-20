# Cancel Subscription with Baremetrics

Cancels a subscription in Baremetrics.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/:source_id/subscriptions/:subscription_oid/cancel`
- **Base URL:** `https://sandbox.baremetrics.com`
- **Official documentation:** [Cancel Subscription](https://developers.baremetrics.com/reference/cancel-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscription_oid` | path | `string` | yes | Your unique ID for the subscription |
| `source_id` | path | `string` | yes | Please see [Sources](ref:sources) |
| `canceled_at` | body | `string` | yes | A unix timestamp of when this subscription was, or should be canceled. |
