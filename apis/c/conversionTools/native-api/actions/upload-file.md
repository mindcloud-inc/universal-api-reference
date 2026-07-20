# Upload File with Conversion Tools

Uploads a new file to Conversion Tools.

## Endpoint

- **Method:** `POST`
- **Path:** `/files`
- **Base URL:** `https://api.conversiontools.io/v1`
- **Official documentation:** [Upload File](https://conversiontools.io/api-documentation#upload-file-to-server)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The file to upload to Conversion Tools. |
