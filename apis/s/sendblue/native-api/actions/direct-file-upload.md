# Direct File Upload with Sendblue

Uploads a file to Sendblue for iMessage attachments.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/upload-file`
- **Base URL:** `https://api.sendblue.co`
- **Official documentation:** [Direct File Upload](https://docs.sendblue.com/api-v2/media/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | File to upload. |
