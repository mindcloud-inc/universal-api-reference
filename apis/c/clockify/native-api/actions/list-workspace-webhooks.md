# List Workspace Webhooks with Clockify

Lists all workspace webhooks in Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/webhooks`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [List Workspace Webhooks](https://docs.developer.clockify.me/#tag/Webhooks/operation/getWebhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `type` | query | `list<string>` | no | Accepted values: `ADDON`, `SYSTEM`, `USER_CREATED`. |
