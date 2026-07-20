# Replace Document with Voiceflow

Replaces a knowledge base document in Voiceflow.

## Endpoint

- **Method:** `PUT`
- **Path:** `https://realtime-api.voiceflow.com/v1alpha1/public/knowledge-base/document/:documentId`
- **Base URL:** `https://general-runtime.voiceflow.com`
- **Official documentation:** [Replace Document](https://docs.voiceflow.com/api-reference/kbpublicapidocument/replace-document)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | ID of the document to target. |
| `data` | body | `object` | yes | Replacement document payload nested under the top-level data field. |
| `maxChunkSize` | query | `number` | no | Optional chunk size in tokens. |
