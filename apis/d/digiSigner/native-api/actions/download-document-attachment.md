# Download Document Attachment with DigiSigner

Downloads a document attachment from DigiSigner by field ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/:documentId/fields/:fieldApiId/attachment`
- **Base URL:** `https://api.digisigner.com/v1`
- **Official documentation:** [Download Document Attachment](https://www.digisigner.com/esignature-api/esignature-api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | DigiSigner document_id that contains the filled attachment field. Use a document from Upload Document, a callback payload, or a signature request response. |
| `fieldApiId` | path | `string` | yes | The api_id of a filled document field where Get Document Fields returns type ATTACHMENT and status FILLED. |
