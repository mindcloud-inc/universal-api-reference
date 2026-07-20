# Upload File with LiveChat

Creates a temporary file upload in LiveChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/upload_file`
- **Base URL:** `https://api.livechatinc.com/v3.6/agent/action`
- **Official documentation:** [Upload File](https://platform.text.com/docs/messaging/agent-chat-api#upload-file)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The file to upload. Maximum 10MB. |
