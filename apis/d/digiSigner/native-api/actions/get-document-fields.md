# Get Document Fields with DigiSigner

Retrieves document fields from DigiSigner by document ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/:documentId/fields`
- **Base URL:** `https://api.digisigner.com/v1`
- **Official documentation:** [Get Document Fields](https://www.digisigner.com/esignature-api/esignature-api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | DigiSigner document_id whose fields should be returned. |
