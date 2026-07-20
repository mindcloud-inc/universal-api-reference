# Create Chat Completion with Ollama

Creates an OpenAI-compatible chat completion in Ollama.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/chat/completions`
- **Base URL:** `https://ollama.com`
- **Official documentation:** [Create Chat Completion](https://docs.ollama.com/api/openai-compatibility)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | — |
| `messages[]` | body | `array<object>` | yes | Array of chat message objects. |
| `temperature` | body | `number` | no | — |
| `max_tokens` | body | `number` | no | — |
| `top_p` | body | `number` | no | — |
| `frequency_penalty` | body | `number` | no | — |
| `presence_penalty` | body | `number` | no | — |
| `response_format` | body | `object` | no | — |
| `stream` | body | `boolean` | no | — |
| `stream_options` | body | `object` | no | — |
| `stop[]` | body | `array<string>` | no | — |
| `tools[]` | body | `array<object>` | no | — |
| `tool_choice` | body | `string` | no | — |
| `reasoning_effort` | body | `string` | no | — |
| `reasoning` | body | `object` | no | — |
| `logit_bias` | body | `object` | no | — |
| `user` | body | `string` | no | — |
| `n` | body | `number` | no | — |
| `seed` | body | `number` | no | — |
