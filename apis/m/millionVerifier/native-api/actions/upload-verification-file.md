# Upload Verification File with MillionVerifier

Uploads a verification file to MillionVerifier.

## Endpoint

- **Method:** `POST`
- **Path:** `https://bulkapi.millionverifier.com/bulkapi/v2/upload`
- **Base URL:** `https://api.millionverifier.com`
- **Official documentation:** [Upload Verification File](https://developer.millionverifier.com/#operation/bulk-upload)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContents` | body | `file` | yes | CSV or text file containing email addresses to verify. |
