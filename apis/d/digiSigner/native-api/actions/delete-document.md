# Delete Document with DigiSigner

Deletes a document from DigiSigner by ID.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/documents/:documentId`
- **Base URL:** `https://api.digisigner.com/v1`
- **Official documentation:** [Delete Document](https://www.digisigner.com/esignature-api/esignature-api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | DigiSigner document_id to delete. |
