# Complete File Upload with Notion

Finalizes a file upload in Notion.

## Endpoint

- **Method:** `POST`
- **Path:** `/file_uploads/:file_upload_id/complete`
- **Base URL:** `https://api.notion.com/v1`
- **Official documentation:** [Complete File Upload](https://developers.notion.com/reference/complete-a-file-upload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_upload_id` | path | `string` | yes | ID of the file upload to complete. |
