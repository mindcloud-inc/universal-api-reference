# Create Chat Completion with OpenRouter

Creates a chat completion in OpenRouter.

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/completions`
- **Base URL:** `https://openrouter.ai/api/v1/`
- **Official documentation:** [Create Chat Completion](https://openrouter.ai/docs/api/api-reference/chat/send-chat-completion-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | OpenRouter model identifier, for example openai/gpt-5.2. |
| `messages[]` | body | `array<object>` | yes | Conversation messages sent to the chat completion endpoint. |
| `messages[].content` | body | `string` | yes | Text content for the message. |
| `temperature` | body | `number` | no | Sampling temperature. |
| `max_tokens` | body | `number` | no | Maximum number of completion tokens. |
| `stream` | body | `boolean` | no | Whether to stream incremental tokens. |
