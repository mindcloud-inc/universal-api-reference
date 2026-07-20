# Create Message with CometAPI

Creates a Claude message in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Create Message](https://www.cometapi.com/claude-opus-4-5-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `max_tokens` | body | `number` | yes | Maximum number of tokens to generate. |
| `messages[]` | body | `array<object>` | yes | Anthropic message turns. |
| `model` | body | `string` | yes | Anthropic-compatible model ID. |
