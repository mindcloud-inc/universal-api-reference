# Search Web with Domain Filter with LLMLayer

Searches the web in LLMLayer with domain filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/web_search`
- **Base URL:** `https://api.llmlayer.dev`
- **Official documentation:** [Search Web with Domain Filter](https://docs.llmlayer.ai/api-reference/endpoint/web-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain_filter[]` | body | `array<string>` | no | Restrict results to one or more domains. |
| `query` | body | `string` | yes | Search query to run against the web. |
