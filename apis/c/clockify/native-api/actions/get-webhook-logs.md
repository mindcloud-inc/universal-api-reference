# Get Webhook Logs with Clockify

Retrieves logs for a webhook from Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/webhooks/:webhookId/logs`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Get Webhook Logs](https://docs.developer.clockify.me/#tag/Webhooks/operation/getLogsForWebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `webhookId` | path | `string<string>` | yes | — |
| `size` | query | `number` | no | — |
| `from` | body | `date` | no | — |
| `sortByNewest` | body | `boolean` | no | — |
| `status` | body | `list<string>` | no | Accepted values: `ALL`, `FAILED`, `SUCCEEDED`. |
| `to` | body | `date` | no | — |
