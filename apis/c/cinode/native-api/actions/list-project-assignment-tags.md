# List Project Assignment Tags with Cinode

Retrieves tags for a project assignment in Cinode.

## Endpoint

- **Method:** `GET`
- **Path:** `/v0.2/companies/:companyId/projects/:projectId/roles/:roleId/tags`
- **Base URL:** `https://api.cinode.com`
- **Official documentation:** [List Project Assignment Tags](https://api.cinode.com/docs/index.html#/ProjectAssignmentTags/GetProjectAssignmentTags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Cinode company identifier. |
| `projectId` | path | `number` | yes | Identifier of the project. |
| `roleId` | path | `number` | yes | Identifier of the project assignment role. |
