# Remove Project Tag with Cinode

Removes a tag from a project in Cinode.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v0.2/companies/:companyId/projects/:projectId/tags/:tagId`
- **Base URL:** `https://api.cinode.com`
- **Official documentation:** [Remove Project Tag](https://api.cinode.com/docs/index.html#/ProjectTags/UntagProjectV02)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Cinode company identifier. |
| `projectId` | path | `number` | yes | Identifier of the project. |
| `tagId` | path | `number` | yes | Identifier of the tag to remove. |
