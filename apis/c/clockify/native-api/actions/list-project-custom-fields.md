# List Project Custom Fields with Clockify

Lists all project custom fields in Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/projects/:projectId/custom-fields`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [List Project Custom Fields](https://docs.developer.clockify.me/#tag/Custom-fields/operation/getCustomFieldsOfProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `projectId` | path | `string<string>` | yes | — |
| `entity-type` | query | `string` | no | — |
| `status` | query | `list<string>` | no | Accepted values: `INACTIVE`, `INVISIBLE`, `VISIBLE`. |
