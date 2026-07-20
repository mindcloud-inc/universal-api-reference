# Apply Code Changes with Morph

Applies code changes with Morph.

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/completions`
- **Base URL:** `https://api.morphllm.com/v1`
- **Official documentation:** [Apply Code Changes](https://docs.morphllm.com/api-reference/endpoint/apply)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[]` | body | `array<object>` | yes | Single-message Apply payload using Morph's required structured format. |
| `temperature` | body | `number` | no | Sampling temperature. Use 0 for deterministic edits. |
| `max_tokens` | body | `number` | no | Maximum number of tokens to generate. |
