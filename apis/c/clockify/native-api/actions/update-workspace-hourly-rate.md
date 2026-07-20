# Update Workspace Hourly Rate with Clockify

Updates a workspace hourly rate in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/hourly-rate`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Workspace Hourly Rate](https://docs.developer.clockify.me/#tag/Workspace/operation/setWorkspaceHourlyRate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `amount` | body | `number` | yes | — |
| `currency` | body | `string` | yes | Maximum length: 100. |
| `since` | body | `string` | no | — |
