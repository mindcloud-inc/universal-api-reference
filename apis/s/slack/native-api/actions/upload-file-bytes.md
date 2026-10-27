# Upload File Bytes with Slack

## Endpoint

- **Method:** `POST`
- **Path:** `https://files.slack.com/upload/v1/:upload_token`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Upload File Bytes](https://docs.slack.dev/reference/methods/files.getUploadURLExternal/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/octet-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `upload_token` | path | `string` | yes | Opaque final path segment from the Slack upload_url returned by Get File Upload URL. |
| `file` | body | `file` | yes | Exact file bytes matching the Length sent to Get File Upload URL; accepts base64 or a file URL. |
