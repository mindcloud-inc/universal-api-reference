# Remove Project Custom Field with Clockify

Removes a project custom field in Clockify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `workspaces/:workspaceId/projects/:projectId/custom-fields/:customFieldId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Remove Project Custom Field](https://docs.developer.clockify.me/#tag/Custom-fields/operation/removeDefaultValueOfProject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `projectId` | path | `string<string>` | yes |
| `customFieldId` | path | `string<string>` | yes |
