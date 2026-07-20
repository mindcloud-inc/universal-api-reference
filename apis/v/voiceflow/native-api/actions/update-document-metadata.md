# Update Document Metadata with Voiceflow

Updates document metadata in Voiceflow's knowledge base.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://realtime-api.voiceflow.com/v1alpha1/public/knowledge-base/document/:documentId`
- **Base URL:** `https://general-runtime.voiceflow.com`
- **Official documentation:** [Update Document Metadata](https://docs.voiceflow.com/api-reference/kbpublicapidocument/update-document-metadata)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | ID of the document to target. |
| `data` | body | `object` | yes | Metadata update payload nested under the top-level data field. |
