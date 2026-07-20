# Create Chat Completion with Grok

Creates a chat completion in Grok.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/chat/completions`
- **Base URL:** `https://api.x.ai`
- **Official documentation:** [Create Chat Completion](https://docs.x.ai/developers/rest-api-reference/inference/chat#chat-completions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | Model ID to use for the chat completion. |
| `messages[]` | body | `array<object>` | yes | — |
