# Search Documents with Voiceflow

Finds knowledge base documents in Voiceflow.

## Endpoint

- **Method:** `GET`
- **Path:** `https://realtime-api.voiceflow.com/v1alpha1/public/knowledge-base/document`
- **Base URL:** `https://general-runtime.voiceflow.com`
- **Official documentation:** [Search Documents](https://docs.voiceflow.com/api-reference/kbpublicapidocument/search-documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number to retrieve. |
| `limit` | query | `number` | no | Number of documents to return per page. |
| `documentType` | query | `string` | no | Filter documents by type. |
