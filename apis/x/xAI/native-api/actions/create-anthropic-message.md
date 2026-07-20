# Create Anthropic Message with xAI

Creates an Anthropic-style message in the xAI API.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages`
- **Base URL:** `https://api.x.ai/v1`
- **Official documentation:** [Create Anthropic Message](https://docs.x.ai/developers/rest-api-reference/inference/legacy#create-messages-response)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | no | Model name to use for the Anthropic-compatible message. |
| `max_tokens` | body | `number` | no | Maximum number of output tokens. |
| `messages[]` | body | `array<object>` | no | Input messages for the Anthropic-compatible request. |
