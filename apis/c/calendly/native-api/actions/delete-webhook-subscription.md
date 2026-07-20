# Delete Webhook Subscription with Calendly

Deletes a webhook subscription from Calendly.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/webhook_subscriptions/:webhook_uuid`
- **Base URL:** `https://api.calendly.com`
- **Official documentation:** [Delete Webhook Subscription](https://developer.calendly.com/receive-data-from-scheduled-events-in-real-time-with-webhook-subscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_uuid` | path | `string` | yes | Webhook subscription UUID. |
