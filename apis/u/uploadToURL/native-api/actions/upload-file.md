# Upload File with Upload to URL

## Endpoint

- **Method:** `POST`
- **Path:** `/api/upload`
- **Base URL:** `https://uploadtourl.com`
- **Official documentation:** [Upload File](https://uploadtourl.com/api-docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The file to upload (multipart form-data). |
| `expiry_days` | body | `string` | no | Number of days before the file expires. Default is 30. |
