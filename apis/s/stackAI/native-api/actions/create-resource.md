# Create Resource with Stack AI

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/knowledge-bases/:knowledge_base_id/resources`
- **Base URL:** `https://api.stack-ai.com`
- **Official documentation:** [Create Resource](https://docs.stackai.com/api-reference/knowledge-bases#post-v1-knowledge-bases-knowledge_base_id-resources)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `knowledge_base_id` | path | `string` | yes | The knowledge base identifier. |
| `file` | body | `file` | yes | The file to upload to the knowledge base. |
