# Download Document with SigningHub

Downloads a document from SigningHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/packages/:packageId/documents/:documentId`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Download Document](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Documents_DownloadDocumentBytes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `number` | yes | The document ID to download. |
| `packageId` | path | `number` | yes | Package ID of the package to which the document belongs. |
