# Add Knowledge Base Text or File Data Sources with QWIC

Adds text or file data sources to a QWIC knowledge base.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/ai/knowledge-base/:knowledge_base_id/upload/sources`
- **Base URL:** `https://app.qwic.ai`
- **Official documentation:** [Add Knowledge Base Text or File Data Sources](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#adding-text-file-data-sources-to-a-knowledge-base)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `knowledge_base_id` | path | `number` | yes | Knowledge base ID. |
| `text_data_source_name` | body | `string` | no | Plain text content to upload as a knowledge base source. |
| `file_data_source_name` | body | `file` | no | File content to upload as a knowledge base source. |
