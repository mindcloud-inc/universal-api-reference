# Update Project Template with Clockify

Updates a project template in Clockify.

## Endpoint

- **Method:** `PATCH`
- **Path:** `workspaces/:workspaceId/projects/:projectId/template`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Project Template](https://docs.developer.clockify.me/#tag/Project/operation/updateIsProjectTemplate)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `projectId` | path | `string<string>` | yes |
| `isTemplate` | body | `boolean` | no |
