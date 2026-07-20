# Upload File with Groq

Uploads a file to Groq.

## Endpoint

- **Method:** `POST`
- **Path:** `/openai/v1/files`
- **Base URL:** `https://api.groq.com`
- **Official documentation:** [Upload File](https://console.groq.com/docs/api-reference#files-upload)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
| `purpose` | body | `list` | yes |
