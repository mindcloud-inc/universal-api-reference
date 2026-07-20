# Create Webhook with Clockify

Creates a new webhook in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/webhooks`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Create Webhook](https://docs.developer.clockify.me/#tag/Webhooks/operation/createWebhook)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `triggerSourceType` | body | `string` | yes |
| `triggerSource[]` | body | `array<string>` | yes |
| `webhookEvent` | body | `string` | yes |
| `url` | body | `string` | yes |
| `name` | body | `string` | no |
