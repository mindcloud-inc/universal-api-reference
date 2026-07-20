# Upload Media with ContentStudio

Creates a media asset in a ContentStudio workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/:workspace_id/media`
- **Base URL:** `https://api.contentstudio.io/api/v1`
- **Official documentation:** [Upload Media](https://api-prod.contentstudio.io/scalar)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | no | Media file to upload. |
| `folder_id` | body | `string` | no | Folder ID to upload into. |
| `url` | body | `string` | no | Remote URL to import media from. |
| `workspace_id` | path | `string` | yes | ContentStudio workspace ID. |
