# Create Webhook with Ghost

Creates a new webhook in Ghost.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/`
- **Base URL:** `{adminDomain}/ghost/api/admin`
- **Official documentation:** [Create Webhook](https://docs.ghost.org/admin-api/webhooks/creating-a-webhook)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `webhooks[0].event` | body | `string` | yes |
| `webhooks[0].target_url` | body | `string` | yes |
| `webhooks[0].name` | body | `string` | no |
| `webhooks[0].secret` | body | `string` | no |
| `webhooks[0].integration_id` | body | `string` | no |
