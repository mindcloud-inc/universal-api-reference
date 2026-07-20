# Remove Project Assignment Tag with Cinode

Removes a tag from a project assignment in Cinode.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v0.2/companies/:companyId/projects/:projectId/roles/:roleId/tags/:tagId`
- **Base URL:** `https://api.cinode.com`
- **Official documentation:** [Remove Project Assignment Tag](https://api.cinode.com/docs/index.html#/ProjectAssignmentTags/UntagProjectAssignment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Cinode company identifier. |
| `projectId` | path | `number` | yes | Identifier of the project. |
| `roleId` | path | `number` | yes | Identifier of the project assignment role. |
| `tagId` | path | `number` | yes | Identifier of the tag to remove. |
