# Update Subscription with Feedbin

Updates an existing subscription in Feedbin.

## Endpoint

- **Method:** `PATCH`
- **Path:** `subscriptions/[:id].json`
- **Base URL:** `https://api.feedbin.com/v2`
- **Official documentation:** [Update Subscription](https://github.com/feedbin/feedbin-api/blob/master/content/subscriptions.md#update-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Feedbin subscription ID. |
| `title` | body | `string` | yes | Custom title for the subscription. |
