# Fetch Knowledge Base Details with QWIC

Retrieves details for a QWIC knowledge base.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/ai/knowledge-base/:knowledge_base_id`
- **Base URL:** `https://app.qwic.ai`
- **Official documentation:** [Fetch Knowledge Base Details](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#fetch-knowledge-base-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `knowledge_base_id` | path | `number` | yes | The knowledge base ID. |
| `limit` | body | `number` | no | The maximum number of data sources to return. |
| `offset` | body | `number` | no | The offset for paginated data sources. |
