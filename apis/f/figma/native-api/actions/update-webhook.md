# Update Webhook with Figma

Updates an existing webhook in Figma.

## Endpoint

- **Method:** `PUT`
- **Path:** `https://api.figma.com/v2/webhooks/:webhook_id`
- **Base URL:** `https://api.figma.com/v1`
- **Official documentation:** [Update Webhook](https://developers.figma.com/docs/rest-api/webhooks-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_id` | path | `string` | yes | Webhook identifier to update. |
| `event_type` | body | `list` | yes | Webhook event to subscribe to. |
| `endpoint` | body | `string` | yes | HTTPS endpoint that receives webhook POST requests. |
| `passcode` | body | `string` | yes | Secret string echoed by Figma webhook calls for verification. |
| `status` | body | `list` | no | Webhook state after update. |
| `description` | body | `string` | no | Optional display name/description for the webhook. |
| `team_id` | body | `string` | no | Deprecated legacy team identifier included due OpenAPI required-list inconsistency. |
