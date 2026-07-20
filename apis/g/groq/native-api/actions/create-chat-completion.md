# Create Chat Completion with Groq

Creates a chat completion in Groq.

## Endpoint

- **Method:** `POST`
- **Path:** `/openai/v1/chat/completions`
- **Base URL:** `https://api.groq.com`
- **Official documentation:** [Create Chat Completion](https://console.groq.com/docs/api-reference#chat-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | The Groq model identifier to use for the chat completion. |
| `messages[]` | body | `array<object>` | yes | The chat messages to send, in order. |
| `max_completion_tokens` | body | `number` | no | Upper bound for generated completion tokens. |
| `temperature` | body | `number` | no | Controls response randomness from 0 to 2. |
| `stream` | body | `boolean` | no | When true, return the completion as a stream. |
| `user` | body | `string` | no | — |
| `reasoning_effort` | body | `list` | no | — |
| `include_reasoning` | body | `boolean` | no | — |
| `reasoning_format` | body | `list` | no | — |
| `citation_options` | body | `list` | no | — |
| `parallel_tool_calls` | body | `boolean` | no | — |
| `seed` | body | `number` | no | — |
| `service_tier` | body | `list` | no | — |
| `top_p` | body | `number` | no | — |
| `logprobs` | body | `boolean` | no | — |
