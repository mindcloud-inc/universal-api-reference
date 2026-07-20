# Create Webhook with Figma

Creates a new webhook in Figma.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.figma.com/v2/webhooks`
- **Base URL:** `https://api.figma.com/v1`
- **Official documentation:** [Create Webhook](https://developers.figma.com/docs/rest-api/webhooks-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_type` | body | `list` | yes | Webhook event to subscribe to. |
| `context` | body | `list` | yes | Webhook context: team, project, or file. |
| `context_id` | body | `string` | yes | ID of the context the webhook is attached to. |
| `endpoint` | body | `string` | yes | HTTPS endpoint that receives webhook POST requests. |
| `passcode` | body | `string` | yes | Secret string echoed by Figma webhook calls for verification. |
| `status` | body | `list` | no | Initial webhook state. |
| `description` | body | `string` | no | Optional display name/description for the webhook. |
| `team_id` | body | `string` | no | Deprecated legacy team identifier; prefer context/context_id. |
