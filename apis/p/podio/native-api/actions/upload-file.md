# Upload File with Podio

Uploads a file to Podio.

## Endpoint

- **Method:** `POST`
- **Path:** `/file/`
- **Base URL:** `https://api.podio.com`
- **Official documentation:** [Upload File](https://developers.podio.com/doc/files/upload-file-1004361)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | body | `file` | yes | The file contents to upload. |
| `filename` | body | `string` | yes | The name of the file. |
