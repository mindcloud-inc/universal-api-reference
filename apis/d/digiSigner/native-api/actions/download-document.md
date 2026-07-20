# Download Document with DigiSigner

Downloads a document from DigiSigner by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/:documentId`
- **Base URL:** `https://api.digisigner.com/v1`
- **Official documentation:** [Download Document](https://www.digisigner.com/esignature-api/esignature-api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | DigiSigner document_id returned by Upload Document or a template ID where the endpoint accepts one. |
