# Search News with LLMLayer

Searches news in LLMLayer for raw results.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/web_search`
- **Base URL:** `https://api.llmlayer.dev`
- **Official documentation:** [Search News](https://docs.llmlayer.ai/api-reference/endpoint/web-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Search query to run against the news index. |
