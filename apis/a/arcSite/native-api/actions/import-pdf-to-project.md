# Import PDF to Project with ArcSite

Imports a PDF as drawings into an ArcSite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/import_pdf`
- **Base URL:** `https://api.arcsite.com/v1`
- **Official documentation:** [Import PDF to Project](https://dev.arcsite.com/#import-pdf)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The ID of the project. |
| `file_url` | body | `string` | yes | Publicly accessible PDF URL to import. |
