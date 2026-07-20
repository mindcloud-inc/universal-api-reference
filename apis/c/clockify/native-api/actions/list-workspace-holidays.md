# List Workspace Holidays with Clockify

Lists all workspace holidays in Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/holidays`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [List Workspace Holidays](https://docs.developer.clockify.me/#tag/Holiday/operation/getHolidays)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `assigned-to` | query | `string` | no |
