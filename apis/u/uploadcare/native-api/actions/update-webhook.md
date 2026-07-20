# Update Webhook with Uploadcare

Updates an existing webhook in Uploadcare.

## Endpoint

- **Method:** `PUT`
- **Path:** `/webhooks/:id/`
- **Base URL:** `https://api.uploadcare.com`
- **Official documentation:** [Update Webhook](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/Webhook/operation/updateWebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | body | `string` | no | Updated Uploadcare event type. |
| `id` | path | `number` | yes | Uploadcare webhook identifier. |
| `is_active` | body | `boolean` | no | Whether the webhook should remain active. |
| `signing_secret` | body | `string` | no | Updated shared secret for webhook signature verification. |
| `target_url` | body | `string` | no | Updated webhook destination URL. |
