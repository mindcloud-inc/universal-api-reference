# Create Webhook with Superchat

Creates a new webhook in Superchat.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.superchat.com/v1.0`
- **Official documentation:** [Create Webhook](https://developers.superchat.com/reference/createwebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target_url` | body | `string` | yes | The target URL for the webhook. Must use `https://` |
| `events[]` | body | `array<object>` | yes | — |
