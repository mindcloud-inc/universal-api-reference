# Update Webhook with Instantly

Updates an existing webhook in Instantly.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/webhooks/:id`
- **Base URL:** `https://api.instantly.ai`
- **Official documentation:** [Update Webhook](https://developer.instantly.ai/api/v2/webhook/patchwebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Webhook UUID. |
| `name` | body | `string` | no | User-defined webhook name. |
| `target_hook_url` | body | `string` | no | Target URL to send webhook payloads. |
| `event_type` | body | `string` | no | Event type to trigger the webhook. |
