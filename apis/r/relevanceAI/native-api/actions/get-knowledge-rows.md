# Retrieve Knowledge Set Rows with Relevance AI

## Endpoint

- **Method:** `POST`
- **Path:** `/knowledge/list`
- **Base URL:** `https://api-{region}.stack.tryrelevance.com/latest`
- **Official documentation:** [Retrieve Knowledge Set Rows](https://sdk.relevanceai.com/concepts/10_1/knowledge)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `knowledge_set` | body | `string` | yes | The knowledge set id to read rows from. |
| `page_size` | body | `number` | no | Maximum number of rows to return. |
