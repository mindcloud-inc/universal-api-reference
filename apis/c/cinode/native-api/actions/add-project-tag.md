# Add Project Tag with Cinode

Adds a tag to a project in Cinode.

## Endpoint

- **Method:** `POST`
- **Path:** `/v0.2/companies/:companyId/projects/:projectId/tags`
- **Base URL:** `https://api.cinode.com`
- **Official documentation:** [Add Project Tag](https://api.cinode.com/docs/index.html#/ProjectTags/TagProjectV02)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Cinode company identifier. |
| `projectId` | path | `number` | yes | Identifier of the project. |
| `id` | body | `number` | no | Existing tag identifier to add. |
| `name` | body | `string` | no | Tag name to create or match. |
