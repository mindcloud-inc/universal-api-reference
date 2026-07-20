# Pause Subscription with Recurly

## Endpoint

- **Method:** `PUT`
- **Path:** `/subscriptions/:subscription_id/pause`
- **Base URL:** `https://v3.recurly.com`
- **Official documentation:** [Pause Subscription](https://recurly.com/developers/api/v2021-02-25/#operation/pause_subscription)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `remaining_pause_cycles` | body | `number` | yes |
| `subscription_id` | path | `string` | yes |
