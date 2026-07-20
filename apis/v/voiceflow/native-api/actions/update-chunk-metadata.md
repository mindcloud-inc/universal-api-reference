# Update Chunk Metadata with Voiceflow

Updates chunk metadata in Voiceflow's knowledge base.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://realtime-api.voiceflow.com/v1alpha1/public/knowledge-base/document/:documentId/chunk/:chunkId`
- **Base URL:** `https://general-runtime.voiceflow.com`
- **Official documentation:** [Update Chunk Metadata](https://docs.voiceflow.com/api-reference/kbpublicapidocument/update-chunk-metadata)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | ID of the document to target. |
| `chunkId` | path | `string` | yes | ID of the document chunk to target. |
| `data` | body | `object` | yes | Chunk metadata update payload nested under the top-level data field. |
