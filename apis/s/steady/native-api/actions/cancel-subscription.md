# Cancel Subscription with Steady

Cancels a Steady subscription at the current term's end.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscriptions/:subscription_id/cancel`
- **Base URL:** `https://steadyhq.com/api/v1`
- **Official documentation:** [Cancel Subscription](https://developers.steadyhq.com/#post-subscriptions-subscription_id-cancel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscription_id` | path | `string` | yes | The Steady subscription ID to cancel. |
