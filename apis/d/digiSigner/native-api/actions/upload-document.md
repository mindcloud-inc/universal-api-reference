# Upload Document with DigiSigner

Uploads a new document to DigiSigner.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents`
- **Base URL:** `https://api.digisigner.com/v1`
- **Official documentation:** [Upload Document](https://www.digisigner.com/esignature-api/esignature-api-documentation/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Document file to upload to DigiSigner. |
