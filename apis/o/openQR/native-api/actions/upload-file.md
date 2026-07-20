# Upload File with OpenQR

Uploads a file to the OpenQR account.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/qr-logos`
- **Base URL:** `https://api.openqr.io/api/v1`
- **Official documentation:** [Upload File](https://docs.openqr.io/#tag/Files/operation/UploadFile)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | PNG or JPEG file to upload, max 5 MB. |
