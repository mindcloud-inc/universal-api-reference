# Create Message with Anthropic

Creates the next message in an Anthropic conversation.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [Create Message](https://platform.claude.com/docs/en/api/messages/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | The model that will complete your prompt. |
| `max_tokens` | body | `number` | yes | The maximum number of tokens to generate before stopping. |
| `messages[]` | body | `array<object>` | yes | Input conversation messages. |
| `temperature` | body | `number` | no | Amount of randomness injected into responses. |
| `top_p` | body | `number` | no | Nucleus sampling parameter. |
| `top_k` | body | `number` | no | Only sample from the top K options. |
| `stream` | body | `boolean` | no | Whether to stream response chunks. |
| `stop_sequences[]` | body | `array<string>` | no | Custom sequences that stop generation. |
