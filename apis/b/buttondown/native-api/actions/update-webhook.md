# Update Webhook with Buttondown

Updates an existing webhook in Buttondown.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/webhooks/:id`
- **Base URL:** `https://api.buttondown.com/v1`
- **Official documentation:** [Update Webhook](https://docs.buttondown.com/api-webhooks-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Webhook ID. |
| `event_types[]` | body | `array<string>` | yes | Exact Buttondown webhook event types to subscribe to. |
| `url` | body | `string` | yes | Destination URL for webhook POST requests. |
| `status` | body | `list` | no | Whether the webhook is enabled or disabled. Accepted values: `disabled`, `enabled`. |
| `description` | body | `string` | no | Optional internal description for the webhook. |
| `signing_key` | body | `string` | no | Optional HMAC signing key for webhook verification. |
