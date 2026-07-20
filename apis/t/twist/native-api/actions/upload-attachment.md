# Upload Attachment with Twist

Uploads a new attachment to Twist.

## Endpoint

- **Method:** `POST`
- **Path:** `/attachments/upload`
- **Base URL:** `https://api.twist.com/api/v3`
- **Official documentation:** [Upload Attachment](https://developer.twist.com/v3/#upload-an-attachment)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attachment_id` | body | `string` | yes | A UUID that will be the id of the attachment. |
| `file_name` | body | `file` | yes | Provide raw base64 file contents or a public file URL. Raw base64 should not include a data:...;base64, prefix. |
