# Text Generation with Minimax

Creates text output in Minimax.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/text/chatcompletion_v2`
- **Base URL:** `https://api.minimax.io`
- **Official documentation:** [Text Generation](https://platform.minimax.io/docs/api-reference/text-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[]` | body | `array<object>` | yes | Conversation messages array sent to MiniMax. |
| `model` | body | `string` | yes | MiniMax model ID to use for the request. |
