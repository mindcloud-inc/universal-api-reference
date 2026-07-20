# Search Web with LLMLayer

Searches the web in LLMLayer for raw results.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/web_search`
- **Base URL:** `https://api.llmlayer.dev`
- **Official documentation:** [Search Web](https://docs.llmlayer.ai/api-reference/endpoint/web-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Search query to run against the web. |
| `search_type` | body | `string` | no | Choose which LLMLayer search index to query. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. |
| `location` | body | `string` | no | Optional location hint for localized results. |
| `recency` | body | `string` | no | Optional recency filter for time-sensitive search types. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `domain_filter` | body | `string` | no | Optional include/exclude domain list. Send multiple values as a array. |
