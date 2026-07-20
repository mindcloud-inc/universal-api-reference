# Send File Upload with Notion

Sends file contents to a Notion upload.

## Endpoint

- **Method:** `POST`
- **Path:** `/file_uploads/:file_upload_id/send`
- **Base URL:** `https://api.notion.com/v1`
- **Official documentation:** [Send File Upload](https://developers.notion.com/reference/send-a-file-upload)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | File content to upload. |
| `file_upload_id` | path | `string` | yes | ID of the file upload to send data to. |
| `part_number` | body | `number` | no | Part number for multipart uploads. |
