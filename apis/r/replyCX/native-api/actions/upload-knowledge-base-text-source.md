# Upload Knowledge Base Text Source with ReplyCX

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/ai/knowledge-base/:knowledge_base_id/upload/sources`
- **Base URL:** `https://api.reply.cx`
- **Official documentation:** [Upload Knowledge Base Text Source](https://help.reply.cx/integrations/public-apis)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `knowledge_base_id` | path | `number` | yes | — |
| `q1` | body | `string` | yes | Text content to upload as one knowledge-base source field. |
