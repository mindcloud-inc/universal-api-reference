# Search Code With WarpGrep with Morph

Searches code with Morph WarpGrep.

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/completions`
- **Base URL:** `https://api.morphllm.com/v1`
- **Official documentation:** [Search Code With WarpGrep](https://docs.morphllm.com/api-reference/endpoint/warpgrep)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[]` | body | `array<object>` | yes | WarpGrep conversation containing the system prompt, user search request, and any tool-call turns. |
| `temperature` | body | `number` | no | Sampling temperature. Use 0 for deterministic search behavior. |
| `max_tokens` | body | `number` | no | Maximum number of tokens to generate per response. |
