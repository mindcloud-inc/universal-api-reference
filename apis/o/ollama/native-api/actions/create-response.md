# Create Response with Ollama

Creates an OpenAI-compatible response in Ollama.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/responses`
- **Base URL:** `https://ollama.com`
- **Official documentation:** [Create Response](https://docs.ollama.com/api/openai-compatibility)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `model` | body | `string` | yes |
| `input` | body | `string` | yes |
| `instructions` | body | `string` | no |
| `tools[]` | body | `array<object>` | no |
| `stream` | body | `boolean` | no |
| `temperature` | body | `number` | no |
| `top_p` | body | `number` | no |
| `max_output_tokens` | body | `number` | no |
| `truncation` | body | `string` | no |
