# Chat Completions with Easy-Peasy.AI

Creates a chat completion in Easy-Peasy.AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/chat/completions`
- **Base URL:** `https://easy-peasy.ai`
- **API:** rest
- **Official documentation:** [Chat Completions](https://docs.easy-peasy.ai/api-reference/endpoint/chat-completions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[]` | body | `array<object>` | yes | The chat message array in OpenAI-compatible format with role and content per item. |
| `model` | body | `string` | no | Optional chat model override such as gpt-4.1-mini. |
| `stream` | body | `boolean` | no | Enable streaming server-sent events. |
| `temperature` | body | `number` | no | Optional sampling temperature from 0 to 2. |
| `max_tokens` | body | `number` | no | Optional maximum number of tokens to generate. |
| `top_p` | body | `number` | no | Optional nucleus sampling parameter. |
