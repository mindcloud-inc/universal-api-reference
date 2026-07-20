# Update Webhook with TimelinesAI

Updates an existing webhook subscription in TimelinesAI.

## Endpoint

- **Method:** `PUT`
- **Path:** `/webhooks/{webhook_id}`
- **Base URL:** `https://app.timelines.ai/integrations/api`
- **Official documentation:** [Update Webhook](https://timelinesai.mintlify.app/public-api-reference/update-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_id` | path | `string` | yes | ID of the webhook in TimelinesAI. |
| `event_type` | body | `string` | no | Webhook event type to subscribe to. |
| `enabled` | body | `boolean` | no | Enable or disable the webhook. |
| `url` | body | `string` | no | Destination URL for webhook deliveries. |
