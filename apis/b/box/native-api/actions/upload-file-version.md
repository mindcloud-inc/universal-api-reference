# Upload File Version with Box

## Endpoint

- **Method:** `POST`
- **Path:** `https://upload.box.com/api/2.0/files/:file_id/content`
- **Base URL:** `https://api.box.com/2.0`
- **Official documentation:** [Upload File Version](https://developer.box.com/reference/post-files-id-content)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | path | `string` | yes | The file ID to upload a new version for. |
| `fileName` | body | `string` | no | Optional replacement filename for the uploaded new version. |
| `file` | body | `file` | yes | Paste a plain base64 string, a full data URL, or a public HTTPS file URL. Data URLs are stripped to raw base64 automatically before upload. |
| `fields` | query | `string` | no | Optional comma-separated list of file fields to include in the response. |
