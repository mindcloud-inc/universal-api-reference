# Create Webhook with Uploadcare

Creates a new webhook in Uploadcare.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/`
- **Base URL:** `https://api.uploadcare.com`
- **Official documentation:** [Create Webhook](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/Webhook/operation/webhookCreate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | body | `string` | yes | Uploadcare event type to subscribe to. |
| `is_active` | body | `boolean` | no | Whether the webhook should be active immediately. |
| `signing_secret` | body | `string` | no | Optional shared secret for webhook signature verification. |
| `target_url` | body | `string` | yes | Webhook destination URL. |
| `version` | body | `string` | no | Webhook payload version. |
