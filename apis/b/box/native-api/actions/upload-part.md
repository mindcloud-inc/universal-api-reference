# Upload Part with Box

## Endpoint

- **Method:** `PUT`
- **URL:** `https://upload.box.com/api/2.0/files/upload_sessions/:session_id`
- **Official documentation:** [Upload Part](https://developer.box.com/reference/put-files-upload-sessions-id)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/octet-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `session_id` | path | `string` | yes | Upload session ID returned by Create Upload Session. |
| `partStart` | body | `number` | yes | Zero-based byte offset where this part starts. |
| `partEnd` | body | `number` | yes | Inclusive byte offset where this part ends. |
| `totalFileSize` | body | `number` | yes | Total size of the complete file in bytes. |
| `file` | body | `file` | yes | Raw base64 content for this part. It is decoded and sent as the naked request body. |
