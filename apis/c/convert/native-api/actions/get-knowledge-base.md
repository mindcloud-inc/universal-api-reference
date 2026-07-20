# Get Knowledge Base Entry with Convert

Retrieves a knowledge base entry from Convert.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:account_id/projects/:project_id/knowledge-bases/:knowledge_base_id`
- **Base URL:** `https://api.convert.com/api/v2`
- **Official documentation:** [Get Knowledge Base Entry](https://api.convert.com/doc/v2/#tag/Knowledge-Bases/operation/getKnowledgeBase)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Convert project ID. |
| `knowledge_base_id` | path | `string` | yes | Convert Knowledge Base entry ID. |
