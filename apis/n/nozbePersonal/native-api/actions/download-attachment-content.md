# Download Attachment Content with Nozbe Personal

Retrieves attachment file content from Nozbe Personal.

## Endpoint

- **Method:** `GET`
- **Path:** `/comments/:comment_id/attachments/:file_id/content`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [Download Attachment Content](https://api4.nozbe.com/v1/api#/attachments/getattachmentByIdContent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comment_id` | path | `string` | yes | Comment ID from Nozbe. |
| `file_id` | path | `string` | yes | Attachment file ID from Nozbe. |
