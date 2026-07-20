# Add Knowledge Base Domain Data Source with QWIC

Adds a domain data source to a QWIC knowledge base.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/ai/knowledge-base/:knowledge_base_id/data-sources/domain`
- **Base URL:** `https://app.qwic.ai`
- **Official documentation:** [Add Knowledge Base Domain Data Source](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#adding-domain-data-source-to-a-knowledge-base)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `knowledge_base_id` | path | `number` | yes | The knowledge base ID. |
| `url` | body | `string` | yes | The domain URL to crawl. |
| `exclude_urls` | body | `string` | no | Optional excluded URLs. |
