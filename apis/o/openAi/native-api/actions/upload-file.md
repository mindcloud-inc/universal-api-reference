# Upload File with Open AI

Uploads a file to Open AI.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/files`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Upload File](https://developers.openai.com/api/reference/resources/files/methods/create)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | File content or file source to upload. |
| `purpose` | body | `list` | yes | Intended purpose of the uploaded file. |
