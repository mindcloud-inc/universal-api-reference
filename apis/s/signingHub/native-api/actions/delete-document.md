# Delete Document with SigningHub

Deletes a document from SigningHub.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v4/packages/:packageId/documents/:documentId`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Delete Document](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Documents_DeleteDocument)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `number` | yes | The document package containing the document to delete. |
| `documentId` | path | `number` | yes | The document to delete. |
