# List Workspace Custom Fields with Clockify

Lists all workspace custom fields in Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/custom-fields`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [List Workspace Custom Fields](https://docs.developer.clockify.me/#tag/Custom-fields/operation/ofWorkspace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `entity-type` | query | `string` | no | — |
| `name` | query | `string` | no | — |
| `status` | query | `list<string>` | no | Accepted values: `INACTIVE`, `INVISIBLE`, `VISIBLE`. |
