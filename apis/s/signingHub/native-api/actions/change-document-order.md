# Change Document Order with SigningHub

Updates document order in SigningHub.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v4/packages/:packageId/documents/:documentId/reorder`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Change Document Order](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Documents_UpdateDocumentOrder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `number` | yes | The document package containing the document to reorder. |
| `documentId` | path | `number` | yes | The document to reorder. |
| `order` | body | `number` | yes | The new document order position. |
