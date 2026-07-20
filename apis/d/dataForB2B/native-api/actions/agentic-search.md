# Agentic Search with DataForB2B

Searches DataForB2B with a prompt.

## Endpoint

- **Method:** `POST`
- **Path:** `/search/llm`
- **Base URL:** `https://api.dataforb2b.ai`
- **Official documentation:** [Agentic Search](https://docs.dataforb2b.ai/api-reference/agent-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Natural-language query to run against DataForB2B. |
| `category` | body | `string` | yes | Search category, such as people or company. |
| `count` | body | `number` | no | Maximum number of results to return. |
