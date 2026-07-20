# Download File with Crowdin

Retrieves a download link for a file in Crowdin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/files/:fileId/download`
- **Base URL:** `https://api.crowdin.com/api/v2`
- **Official documentation:** [Download File](https://support.crowdin.com/developer/api/v2/#operation/api.projects.files.download.get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `fileId` | path | `number` | yes |
