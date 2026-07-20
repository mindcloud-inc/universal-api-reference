# Edit File with Crowdin

Updates an existing file in a Crowdin project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:projectId/files/:fileId`
- **Base URL:** `https://api.crowdin.com/api/v2`
- **Official documentation:** [Edit File](https://support.crowdin.com/developer/api/v2/#operation/api.projects.files.patch)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `fileId` | path | `number` | yes |
| `operations[]` | body | `array<object>` | yes |
