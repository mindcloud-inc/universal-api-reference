# Query Knowledge Base with Griptape

Queries a knowledge base in Griptape.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/knowledge-bases/:knowledge_base_id/query`
- **Base URL:** `https://cloud.griptape.ai`
- **Official documentation:** [Query Knowledge Base](https://docs.griptape.ai/stable/griptape-cloud/knowledge-bases/accessing-data/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `knowledge_base_id` | path | `string` | yes | The knowledge base ID to query. |
| `query` | body | `string` | yes | The search query to run against the knowledge base. |
