# Generate Webhook Token with Clockify

Generates a new webhook token in Clockify.

## Endpoint

- **Method:** `PATCH`
- **Path:** `workspaces/:workspaceId/webhooks/:webhookId/token`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Generate Webhook Token](https://docs.developer.clockify.me/#tag/Webhooks/operation/generateNewToken)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `webhookId` | path | `string<string>` | yes |
