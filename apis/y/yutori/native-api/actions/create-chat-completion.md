# Create Chat Completion with Yutori

Creates a chat completion in Yutori.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/chat/completions`
- **Base URL:** `https://api.yutori.com`
- **Official documentation:** [Create Chat Completion](https://docs.yutori.com/reference/browser-use)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[]` | body | `array<object>` | yes | Array of chat messages to send. |
| `model` | body | `string` | no | Yutori model name. |
| `max_completion_tokens` | body | `number` | no | — |
| `temperature` | body | `number` | no | — |
| `top_p` | body | `number` | no | — |
