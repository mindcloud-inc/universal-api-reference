# List User Groups with Clockify

Lists all user groups in Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/user-groups`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [List User Groups](https://docs.developer.clockify.me/#tag/Group/operation/getUserGroups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeTeamManagers` | query | `boolean` | no | — |
| `name` | query | `string` | no | — |
| `page` | query | `number` | no | — |
| `page-size` | query | `number` | no | — |
| `project-id` | query | `string` | no | — |
| `sort-column` | query | `list` | no | Accepted values: `ID`, `NAME`. |
| `sort-order` | query | `list` | no | Accepted values: `ASCENDING`, `DESCENDING`. |
| `workspaceId` | path | `list<string>` | yes | — |
