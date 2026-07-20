# Search Website URLs with LLMLayer

Finds website URLs in LLMLayer by search term.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/map`
- **Base URL:** `https://api.llmlayer.dev`
- **Official documentation:** [Search Website URLs](https://docs.llmlayer.ai/api-reference/endpoint/map)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Website URL to map. |
| `search` | body | `string` | yes | Term to match inside mapped website URLs. |
