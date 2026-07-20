# Add Knowledge Base Domain Source with WotNot

Adds a domain source to a WotNot knowledge base.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/ai/knowledge-base/:knowledge_base_id/data-sources/domain`
- **Base URL:** `https://api.wotnot.io`
- **Official documentation:** [Add Knowledge Base Domain Source](https://help.wotnot.io/build/integrations/public-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `knowledge_base_id` | path | `number` | yes | Knowledge base ID |
| `url` | body | `string` | yes | Domain URL to crawl |
| `exclude_urls` | body | `string` | no | Optional URLs to exclude |
| `refresh_frequency` | body | `string` | no | Optional refresh frequency |
