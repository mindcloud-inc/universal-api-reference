# Create Anthropic Message with Ollama

Creates an Anthropic-compatible message in Ollama.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages`
- **Base URL:** `https://ollama.com`
- **Official documentation:** [Create Anthropic Message](https://docs.ollama.com/api/anthropic-compatibility)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | — |
| `max_tokens` | body | `number` | yes | — |
| `messages[]` | body | `array<object>` | yes | Array of message objects. |
| `system` | body | `string` | no | — |
| `stream` | body | `boolean` | no | — |
| `temperature` | body | `number` | no | — |
| `top_p` | body | `number` | no | — |
| `top_k` | body | `number` | no | — |
| `stop_sequences[]` | body | `array<string>` | no | — |
| `tools[]` | body | `array<object>` | no | — |
| `thinking` | body | `object` | no | — |
