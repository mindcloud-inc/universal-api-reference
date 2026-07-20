# Add Directory with Crowdin

Creates a new directory in a Crowdin project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/directories`
- **Base URL:** `https://api.crowdin.com/api/v2`
- **Official documentation:** [Add Directory](https://support.crowdin.com/developer/api/v2/#operation/api.projects.directories.post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `name` | body | `string` | yes |
| `branchId` | body | `number` | no |
| `directoryId` | body | `number` | no |
| `title` | body | `string` | no |
| `exportPattern` | body | `string` | no |
| `priority` | body | `string` | no |
