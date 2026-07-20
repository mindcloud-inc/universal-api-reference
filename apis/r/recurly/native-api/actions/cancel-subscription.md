# Cancel Subscription with Recurly

## Endpoint

- **Method:** `PUT`
- **Path:** `/subscriptions/:subscription_id/cancel`
- **Base URL:** `https://v3.recurly.com`
- **Official documentation:** [Cancel Subscription](https://recurly.com/developers/api/v2021-02-25/#operation/cancel_subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscription_id` | path | `string` | yes | — |
| `timeframe` | body | `string` | no | Accepted values: `0`, `1`. |
