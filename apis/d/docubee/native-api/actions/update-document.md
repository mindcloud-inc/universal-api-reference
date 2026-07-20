# Update Document with Docubee

Updates an existing document in Docubee.

## Endpoint

- **Method:** `PUT`
- **Path:** `/documents/:documentId`
- **Base URL:** `https://docubee.app/api/v2`
- **Official documentation:** [Update Document](https://docs.docubee.app/#update-existing-document)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/pdf` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contentType` | body | `string` | no | The MIME type of the replacement document. Defaults to application/pdf. |
| `documentId` | path | `string` | no | The Docubee document ID. |
| `fileContentBase64` | body | `string` | no | The replacement document file content encoded as base64. |
