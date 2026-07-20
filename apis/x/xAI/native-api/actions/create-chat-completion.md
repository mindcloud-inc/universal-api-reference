# Create Chat Completion with xAI

Creates a chat completion in the xAI API.

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/completions`
- **Base URL:** `https://api.x.ai/v1`
- **Official documentation:** [Create Chat Completion](https://docs.x.ai/developers/rest-api-reference/inference/chat#create-chat-completion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | no | Model name to use for the chat completion. |
| `messages[]` | body | `array<object>` | no | Conversation messages for the chat completion. |
| `max_completion_tokens` | body | `number` | no | Upper bound for generated visible output tokens. |
