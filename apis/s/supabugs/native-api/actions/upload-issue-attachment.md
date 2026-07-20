# Upload Issue Attachment with Supabugs

Uploads a new attachment to a Supabugs issue.

## Endpoint

- **Method:** `POST`
- **Path:** `/issues/:id/upload-attachments`
- **Base URL:** `https://api.supabugs.io/api/public/v1`
- **Official documentation:** [Upload Issue Attachment](https://api.supabugs.io/api/public/v1/docs/index.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Supabugs issue id. |
| `attachments` | body | `file` | yes | Base64 file content or an https URL to the attachment file. |
