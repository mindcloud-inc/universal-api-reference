# Create Chat Completion with SEA-LION AI Playground

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/completions`
- **Base URL:** `https://api.sea-lion.ai/v1`
- **Official documentation:** [Create Chat Completion](https://docs.sea-lion.ai/guides/inferencing/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `model` | body | `string` | yes |
| `messages[]` | body | `array<object>` | yes |
| `messages[].content` | body | `string` | yes |
| `messages[].role` | body | `string` | yes |
| `temperature` | body | `number` | no |
| `max_tokens` | body | `number` | no |
| `stream` | body | `boolean` | no |
