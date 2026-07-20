# Upload Files with GatherContent

Uploads a file to a GatherContent project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/files`
- **Base URL:** `https://api.gathercontent.com`
- **Official documentation:** [Upload Files](https://docs.gathercontent.com/reference/upload-filed)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | File upload payload. |
| `project_id` | path | `string` | yes | Project id. |
