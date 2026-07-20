# Update Knowledge Base with Stack AI

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/knowledge-bases/:knowledge_base_id`
- **Base URL:** `https://api.stack-ai.com`
- **Official documentation:** [Update Knowledge Base](https://docs.stackai.com/api-reference/knowledge-bases#patch-v1-knowledge-bases-knowledge_base_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `knowledge_base_id` | path | `string` | yes | The knowledge base identifier. |
| `name` | body | `string` | no | The knowledge base name. |
| `description` | body | `string` | no | The knowledge base description. |
