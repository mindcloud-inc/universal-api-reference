# Upload File with Xodo Sign

Uploads a file to Xodo Sign.

## Endpoint

- **Method:** `POST`
- **Path:** `/file`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [Upload File](https://eversign.com/api/documentation/methods#upload-file)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | query | `string` | yes | The Xodo Sign business ID that owns the uploaded file. |
| `upload` | body | `file` | yes | The file to upload as multipart form-data. |
