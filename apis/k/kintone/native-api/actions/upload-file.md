# Upload File with Kintone

Uploads a file to Kintone.

## Endpoint

- **Method:** `POST`
- **Path:** `/file.json`
- **Base URL:** `{baseUrl}/k/v1`
- **Official documentation:** [Upload File](https://kintone.dev/en/docs/kintone/rest-api/files/upload-file/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The file content to upload to Kintone. |
