# Add Project Assignment Tag with Cinode

Adds a tag to a project assignment in Cinode.

## Endpoint

- **Method:** `POST`
- **Path:** `/v0.2/companies/:companyId/projects/:projectId/roles/:roleId/tags`
- **Base URL:** `https://api.cinode.com`
- **Official documentation:** [Add Project Assignment Tag](https://api.cinode.com/docs/index.html#/ProjectAssignmentTags/TagProjectAssignment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Cinode company identifier. |
| `projectId` | path | `number` | yes | Identifier of the project. |
| `roleId` | path | `number` | yes | Identifier of the project assignment role. |
| `id` | body | `number` | no | Existing tag identifier to add. |
| `name` | body | `string` | no | Tag name to create or match. |
