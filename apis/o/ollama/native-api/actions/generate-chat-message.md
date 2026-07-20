# Generate Chat Message with Ollama

Generates the next chat message in Ollama.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/chat`
- **Base URL:** `https://ollama.com`
- **Official documentation:** [Generate Chat Message](https://docs.ollama.com/api/chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | — |
| `messages[]` | body | `array<object>` | yes | Array of chat message objects. |
| `tools[]` | body | `array<object>` | no | Function tools the model may call during chat. |
| `format` | body | `string` | no | Use json or provide a JSON schema object for structured output. |
| `options` | body | `object` | no | — |
| `stream` | body | `boolean` | no | — |
| `think` | body | `string` | no | Use true or false, or high/medium/low for supported models. |
| `keep_alive` | body | `string` | no | — |
| `logprobs` | body | `boolean` | no | — |
