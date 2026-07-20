# Search Knowledge Base Articles with GrooveHQ

Searches public knowledge base articles in GrooveHQ.

## Endpoint

- **Method:** `GET`
- **Path:** `/kb/public/:knowledgeBaseId/articles/search`
- **Base URL:** `https://api.groovehq.com/v1`
- **Official documentation:** [Search Knowledge Base Articles](https://doc.groovehq.com/knowledge-bases)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `keyword` | query | `string` | no |
| `knowledge_base_id` | path | `string` | no |
| `page` | query | `string` | no |
| `per_page` | query | `string` | no |
