# Get File with Crowdin

Retrieves a file from a Crowdin project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/files/:fileId`
- **Base URL:** `https://api.crowdin.com/api/v2`
- **Official documentation:** [Get File](https://support.crowdin.com/developer/api/v2/#operation/api.projects.files.get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `fileId` | path | `number` | yes |
