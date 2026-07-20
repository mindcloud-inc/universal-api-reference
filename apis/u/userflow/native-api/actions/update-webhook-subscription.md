# Update Webhook Subscription with Userflow

Updates an existing webhook subscription in Userflow.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/webhook_subscriptions/:webhook_subscription_id`
- **Base URL:** `https://api.userflow.com`
- **Official documentation:** [Update Webhook Subscription](https://docs.userflow.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `disabled` | body | `boolean` | no | Whether the webhook subscription is disabled. |
| `topics[]` | body | `array<string>` | no | Updated webhook topics. |
| `url` | body | `string` | no | Updated webhook destination URL. |
| `webhook_subscription_id` | path | `string` | yes | ID of the webhook subscription to update. |
