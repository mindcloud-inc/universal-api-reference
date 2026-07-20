# Get Webhook with Clockify

Retrieves a specific webhook from Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/webhooks/:webhookId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Get Webhook](https://docs.developer.clockify.me/#tag/Webhooks/operation/getWebhook)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `webhookId` | path | `string<string>` | yes |
