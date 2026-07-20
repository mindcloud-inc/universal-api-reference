# Upload Attachment With Content with Nozbe Personal

Uploads file content to create a Nozbe Personal attachment.

## Endpoint

- **Method:** `POST`
- **Path:** `/comments/:comment_id/attachment_with_content`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [Upload Attachment With Content](https://api4.nozbe.com/v1/api#/attachments/postattachmentByIdContent2)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comment_id` | path | `string` | yes | Comment ID to attach the file to. |
| `file` | body | `file` | yes | Binary file content to upload. |
