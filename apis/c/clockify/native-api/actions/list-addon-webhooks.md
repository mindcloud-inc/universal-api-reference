# List Addon Webhooks with Clockify

Lists all addon webhooks in Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/addons/:addonId/webhooks`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [List Addon Webhooks](https://docs.developer.clockify.me/#tag/Webhooks/operation/getAddonWebhooks)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `addonId` | path | `string` | yes |
