# Delete Webhook Subscription with Userflow

Deletes an existing webhook subscription from Userflow.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/webhook_subscriptions/:webhook_subscription_id`
- **Base URL:** `https://api.userflow.com`
- **Official documentation:** [Delete Webhook Subscription](https://docs.userflow.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_subscription_id` | path | `string` | yes | ID of the webhook subscription to delete. |
