# Create Webhook with TimelinesAI

Creates a new webhook subscription in TimelinesAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://app.timelines.ai/integrations/api`
- **Official documentation:** [Create Webhook](https://timelinesai.mintlify.app/public-api-reference/create-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_type` | body | `string` | yes | Webhook event type to subscribe to. |
| `enabled` | body | `boolean` | no | Enable or disable the webhook. |
| `url` | body | `string` | yes | Destination URL for webhook deliveries. |
