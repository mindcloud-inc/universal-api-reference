# Create Document with Voiceflow

Creates a knowledge base document in Voiceflow.

## Endpoint

- **Method:** `POST`
- **Path:** `https://realtime-api.voiceflow.com/v1alpha1/public/knowledge-base/document`
- **Base URL:** `https://general-runtime.voiceflow.com`
- **Official documentation:** [Create Document](https://docs.voiceflow.com/api-reference/kbpublicapidocument/create-document)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Document source payload nested under the top-level data field. |
| `maxChunkSize` | query | `number` | no | Chunk size in tokens. |
| `overwrite` | query | `boolean` | no | Overwrite an existing document with the same name. |
| `markdownConversion` | query | `boolean` | no | Convert HTML to markdown before chunking. |
| `llmBasedChunks` | query | `boolean` | no | Use LLM-based chunking. |
| `llmGeneratedQ` | query | `boolean` | no | Prepend LLM-generated retrieval questions to chunks. |
| `llmContentSummarization` | query | `boolean` | no | Summarize content with an LLM before indexing. |
| `llmPrependContext` | query | `boolean` | no | Prepend LLM-generated chunk context. |
| `llmVision` | query | `boolean` | no | Use vision support when extracting document content. |
