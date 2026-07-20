# Chat Completion with Mistral AI

Creates a chat completion in Mistral AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/chat/completions`
- **Base URL:** `https://api.mistral.ai`
- **Official documentation:** [Chat Completion](https://docs.mistral.ai/api/endpoint/chat#operation-chat_completion_v1_chat_completions_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | — |
| `messages[]` | body | `array<object>` | yes | Conversation messages array |
| `temperature` | body | `number` | no | — |
| `top_p` | body | `number` | no | — |
| `max_tokens` | body | `number` | no | — |
| `stream` | body | `boolean` | no | — |
| `stop` | body | `string` | no | — |
| `random_seed` | body | `number` | no | — |
| `safe_prompt` | body | `boolean` | no | — |
| `prompt_mode` | body | `string` | no | — |
| `response_format` | body | `object` | no | Structured output format settings |
| `tools[]` | body | `array<object>` | no | Tool definitions available to the model |
| `tool_choice` | body | `string` | no | — |
| `parallel_tool_calls` | body | `boolean` | no | — |
| `guardrails[]` | body | `array<object>` | no | Guardrail configuration list |
| `metadata` | body | `object` | no | — |
| `prediction` | body | `object` | no | — |
| `presence_penalty` | body | `number` | no | — |
| `frequency_penalty` | body | `number` | no | — |
| `n` | body | `number` | no | — |
