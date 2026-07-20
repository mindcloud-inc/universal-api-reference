# Rename Document with SigningHub

Renames a document in SigningHub.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v4/packages/:packageId/documents/:documentId`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Rename Document](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Documents_RenameDocument)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `number` | yes | The document package containing the document to rename. |
| `documentId` | path | `number` | yes | The document to rename. |
| `document_name` | body | `string` | yes | The new document name. |
