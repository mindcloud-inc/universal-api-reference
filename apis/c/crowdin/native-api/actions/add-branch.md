# Add Branch with Crowdin

Creates a new branch in a Crowdin project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/branches`
- **Base URL:** `https://api.crowdin.com/api/v2`
- **Official documentation:** [Add Branch](https://support.crowdin.com/developer/api/v2/#operation/api.projects.branches.post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `name` | body | `string` | yes |
| `title` | body | `string` | no |
| `exportPattern` | body | `string` | no |
| `priority` | body | `string` | no |
