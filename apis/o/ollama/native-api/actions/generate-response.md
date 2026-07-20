# Generate Response with Ollama

Generates a response from an Ollama model.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/generate`
- **Base URL:** `https://ollama.com`
- **Official documentation:** [Generate Response](https://docs.ollama.com/api/generate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | — |
| `prompt` | body | `string` | yes | — |
| `suffix` | body | `string` | no | Text that appears after the prompt for fill-in-the-middle generation. |
| `images[]` | body | `array<string>` | no | Base64-encoded images for models that support image input. |
| `format` | body | `string` | no | Use json or provide a JSON schema object for structured output. |
| `system` | body | `string` | no | — |
| `options` | body | `object` | no | — |
| `stream` | body | `boolean` | no | — |
| `think` | body | `string` | no | Use true or false, or high/medium/low for supported models. |
| `raw` | body | `boolean` | no | — |
| `keep_alive` | body | `string` | no | — |
| `logprobs` | body | `boolean` | no | — |
| `top_logprobs` | body | `number` | no | — |
