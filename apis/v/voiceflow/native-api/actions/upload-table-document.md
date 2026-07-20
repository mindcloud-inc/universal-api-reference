# Upload Table Document with Voiceflow

Uploads a table document to Voiceflow's knowledge base.

## Endpoint

- **Method:** `POST`
- **Path:** `https://realtime-api.voiceflow.com/v1alpha1/public/knowledge-base/document/upload/table`
- **Base URL:** `https://general-runtime.voiceflow.com`
- **Official documentation:** [Upload Table Document](https://docs.voiceflow.com/api-reference/kbpublicapidocument/upload-table-document)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Table upload payload including the table name, items, schema, and optional folder ID. |
| `overwrite` | query | `boolean` | no | Overwrite an existing table with the same name. |
| `markdownConversion` | query | `boolean` | no | Convert HTML to markdown before chunking. |
| `llmBasedChunks` | query | `boolean` | no | Use LLM-based chunking. |
| `llmGeneratedQ` | query | `boolean` | no | Prepend LLM-generated retrieval questions to chunks. |
| `llmContentSummarization` | query | `boolean` | no | Summarize content with an LLM before indexing. |
| `llmPrependContext` | query | `boolean` | no | Prepend LLM-generated chunk context. |
| `llmVision` | query | `boolean` | no | Use vision support when extracting document content. |
