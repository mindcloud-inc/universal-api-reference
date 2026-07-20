# Update Webhook with Superchat

Updates an existing webhook in Superchat.

## Endpoint

- **Method:** `PUT`
- **Path:** `/webhooks/{webhook_id}`
- **Base URL:** `https://api.superchat.com/v1.0`
- **Official documentation:** [Update Webhook](https://developers.superchat.com/reference/updatewebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_id` | path | `string` | yes | The unique identifier of the webhook |
| `target_url` | body | `string` | yes | The target URL for the webhook. Must use `https://` |
| `events[]` | body | `array<object>` | yes | — |
