# Delete Knowledge Base Data Sources with WotNot

Deletes data sources from a WotNot knowledge base.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/ai/knowledge-bases/:knowledge_base_id/data-sources`
- **Base URL:** `https://api.wotnot.io`
- **Official documentation:** [Delete Knowledge Base Data Sources](https://help.wotnot.io/build/integrations/public-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `knowledge_base_id` | path | `number` | yes | Knowledge base ID |
| `data_sources[0]` | body | `number` | yes | First data source ID to delete |
