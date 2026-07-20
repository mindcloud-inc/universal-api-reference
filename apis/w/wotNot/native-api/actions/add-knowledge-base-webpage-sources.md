# Add Knowledge Base Webpage Sources with WotNot

Adds webpage sources to a WotNot knowledge base.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/ai/knowledge-base/:knowledge_base_id/data-sources/webpages`
- **Base URL:** `https://api.wotnot.io`
- **Official documentation:** [Add Knowledge Base Webpage Sources](https://help.wotnot.io/build/integrations/public-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `knowledge_base_id` | path | `number` | yes | Knowledge base ID |
| `urls[0]` | body | `string` | yes | First webpage URL |
