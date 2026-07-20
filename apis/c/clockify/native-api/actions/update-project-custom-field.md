# Update Project Custom Field with Clockify

Updates a project custom field in Clockify.

## Endpoint

- **Method:** `PATCH`
- **Path:** `workspaces/:workspaceId/projects/:projectId/custom-fields/:customFieldId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Project Custom Field](https://docs.developer.clockify.me/#tag/Custom-fields/operation/editProjectCustomFieldDefaultValue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `projectId` | path | `string<string>` | yes | — |
| `customFieldId` | path | `string<string>` | yes | — |
| `defaultValue` | body | `object` | no | — |
| `status` | body | `list<string>` | no | Accepted values: `INACTIVE`, `INVISIBLE`, `VISIBLE`. |
