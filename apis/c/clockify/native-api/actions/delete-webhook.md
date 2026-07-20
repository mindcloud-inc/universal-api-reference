# Delete Webhook with Clockify

Deletes an existing webhook from Clockify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `workspaces/:workspaceId/webhooks/:webhookId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Delete Webhook](https://docs.developer.clockify.me/#tag/Webhooks/operation/deleteWebhook)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `webhookId` | path | `string<string>` | yes |
