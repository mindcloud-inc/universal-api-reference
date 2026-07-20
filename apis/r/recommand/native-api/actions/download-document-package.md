# Download Document Package with Recommand

Downloads a document package from Recommand.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/documents/:documentId/download-package`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Download Document Package](https://recommand.eu/en/reference/documents/download-document-package)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | documentId parameter. |
| `generatePdf` | query | `string` | no | generatePdf parameter. |
