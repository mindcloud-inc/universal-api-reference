# Update Document with SigningHub

Updates a document in SigningHub.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v4/packages/:packageId/documents/:documentId/update`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Update Document](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Documents_UpdateDocument)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/octet-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `number` | yes | The document package containing the document to replace. |
| `documentId` | path | `number` | yes | The document to replace. |
| `file (binary Stream)` | body | `string` | yes | The replacement raw binary document content. |
