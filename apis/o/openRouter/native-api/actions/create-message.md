# Create Message with OpenRouter

Creates a message response in OpenRouter.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages`
- **Base URL:** `https://openrouter.ai/api/v1/`
- **Official documentation:** [Create Message](https://openrouter.ai/docs/api/api-reference/anthropic-messages/create-messages)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `model` | body | `string` | yes |
| `messages[]` | body | `array<object>` | yes |
| `messages[].content` | body | `string` | yes |
| `temperature` | body | `number` | no |
| `max_tokens` | body | `number` | no |
| `stream` | body | `boolean` | no |
| `system` | body | `string` | no |
