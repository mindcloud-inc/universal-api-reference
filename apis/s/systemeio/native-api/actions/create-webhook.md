# Create Webhook with Systeme.io

Creates a new webhook in Systeme.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/webhooks`
- **Base URL:** `https://api.systeme.io`
- **Official documentation:** [Create Webhook](https://developer.systeme.io/reference/api_webhooks_post-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Webhook name |
| `secret` | body | `string` | yes | Webhook secret |
| `url` | body | `string` | yes | Webhook destination URL |
| `subscriptions[]` | body | `array<string>` | yes | Webhook event subscriptions Send multiple values as a array. |
| `active` | body | `boolean` | no | Whether the webhook is active |
