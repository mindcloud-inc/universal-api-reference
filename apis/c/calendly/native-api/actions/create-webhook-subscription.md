# Create Webhook Subscription with Calendly

Creates a webhook subscription in Calendly.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhook_subscriptions`
- **Base URL:** `https://api.calendly.com`
- **Official documentation:** [Create Webhook Subscription](https://developer.calendly.com/receive-data-from-scheduled-events-in-real-time-with-webhook-subscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | HTTPS endpoint to receive webhook deliveries. |
| `events[]` | body | `array<string>` | yes | Webhook event list. |
| `organization` | body | `string` | yes | Organization URI for webhook scope. |
| `scope` | body | `string` | yes | Subscription scope (organization or user). |
| `user` | body | `string` | no | User URI when using user scope. |
