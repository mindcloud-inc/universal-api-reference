# Search Images with LLMLayer

Searches images in LLMLayer for raw results.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/web_search`
- **Base URL:** `https://api.llmlayer.dev`
- **Official documentation:** [Search Images](https://docs.llmlayer.ai/api-reference/endpoint/web-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Search query to run against image results. |
