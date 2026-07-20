# Count Message Tokens with CometAPI

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages/count_tokens`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Count Message Tokens](https://www.cometapi.com/claude-opus-4-5-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[]` | body | `array<object>` | yes | Anthropic message turns to count. |
| `model` | body | `string` | yes | Anthropic-compatible model ID. |
