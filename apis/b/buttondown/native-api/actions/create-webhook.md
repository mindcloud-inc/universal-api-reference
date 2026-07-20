# Create Webhook with Buttondown

Creates a new webhook in Buttondown.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.buttondown.com/v1`
- **Official documentation:** [Create Webhook](https://docs.buttondown.com/api-webhooks-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_types[]` | body | `array<string>` | yes | Exact Buttondown webhook event types to subscribe to. |
| `url` | body | `string` | yes | Destination URL for webhook POST requests. |
| `status` | body | `list` | no | Whether the webhook is enabled or disabled. Accepted values: `disabled`, `enabled`. |
| `description` | body | `string` | no | Optional internal description for the webhook. |
| `signing_key` | body | `string` | no | Optional HMAC signing key for webhook verification. |
