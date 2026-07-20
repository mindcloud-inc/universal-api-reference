# Add Knowledge Base Individual URL Data Sources with QWIC

Adds webpage data sources to a QWIC knowledge base.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/ai/knowledge-base/:knowledge_base_id/data-sources/webpages`
- **Base URL:** `https://app.qwic.ai`
- **Official documentation:** [Add Knowledge Base Individual URL Data Sources](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#adding-individual-urls-data-sources-to-a-knowledge-base)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `knowledge_base_id` | path | `number` | yes | The knowledge base ID. |
| `urls[]` | body | `array<string>` | yes | The webpage URLs to add as data sources. |
