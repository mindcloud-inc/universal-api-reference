# Upload File with Heyy

Uploads a file to a Heyy workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/upload_file`
- **Base URL:** `https://api.heyy.io/api/v2.0/`
- **Official documentation:** [Upload File](https://docs.heyy.io/api-reference/upload-file)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The file content to upload. |
| `format` | body | `string` | yes | Optional upload format override. |
