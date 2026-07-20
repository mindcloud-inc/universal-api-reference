# Upload Document with Docubee

Uploads a new document to Docubee.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents`
- **Base URL:** `https://docubee.app/api/v2`
- **Official documentation:** [Upload Document](https://docs.docubee.app/#upload)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/pdf` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contentType` | body | `string` | no | The MIME type of the uploaded document. Defaults to application/pdf. |
| `fileContentBase64` | body | `string` | no | The document file content encoded as base64. |
