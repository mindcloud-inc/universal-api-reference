# Create Webhook with Instantly

Creates a new webhook in Instantly.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/webhooks`
- **Base URL:** `https://api.instantly.ai`
- **Official documentation:** [Create Webhook](https://developer.instantly.ai/api/v2/webhook/createwebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target_hook_url` | body | `string` | yes | Target URL to send webhook payloads. |
| `name` | body | `string` | no | User-defined webhook name. |
| `event_type` | body | `string` | no | Event type to trigger the webhook, such as all_events or email_sent. |
