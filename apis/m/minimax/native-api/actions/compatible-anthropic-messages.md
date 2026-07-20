# Compatible Anthropic Messages with Minimax

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/text/chatcompletion_v2`
- **Base URL:** `https://api.minimax.io`
- **Official documentation:** [Compatible Anthropic Messages](https://platform.minimax.io/docs/api-reference/text-anthropic-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `max_tokens` | body | `number` | yes | Maximum number of tokens to generate. |
| `messages[]` | body | `array<object>` | yes | Conversation messages array sent to MiniMax. |
| `model` | body | `string` | yes | MiniMax model ID to use for the request. |
