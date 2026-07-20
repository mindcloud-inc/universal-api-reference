# List Project Tags with Cinode

Retrieves tags for a project in Cinode.

## Endpoint

- **Method:** `GET`
- **Path:** `/v0.2/companies/:companyId/projects/:projectId/tags`
- **Base URL:** `https://api.cinode.com`
- **Official documentation:** [List Project Tags](https://api.cinode.com/docs/index.html#/ProjectTags/GetProjectTagsV02)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Cinode company identifier. |
| `projectId` | path | `number` | yes | Identifier of the project. |
