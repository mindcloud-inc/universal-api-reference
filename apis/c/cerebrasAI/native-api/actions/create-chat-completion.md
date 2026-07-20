# Create Chat Completion with Cerebras AI

Creates a chat completion in Cerebras AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/chat/completions`
- **Base URL:** `https://api.cerebras.ai`
- **Official documentation:** [Create Chat Completion](https://inference-docs.cerebras.ai/api-reference/chat-completions)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `model` | body | `string` | yes |
| `messages[]` | body | `array<object>` | yes |
