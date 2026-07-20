# Generate Text with Easy-Peasy.AI

Generates text in Easy-Peasy.AI from a preset.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/generate`
- **Base URL:** `https://easy-peasy.ai`
- **API:** rest
- **Official documentation:** [Generate Text](https://docs.easy-peasy.ai/api-reference/endpoint/generate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `preset` | body | `string` | yes | The preset slug or identifier used for text generation. |
| `keywords` | body | `string` | yes | The prompt keywords or source text used to generate output. |
| `tone` | body | `string` | no | Optional tone to apply to the generated text. |
| `length` | body | `string` | no | Optional output length preference. |
| `outputs` | body | `number` | no | Optional number of generated outputs to return. |
| `language` | body | `string` | no | Optional target language for generated text. |
| `shouldUseGPT4` | body | `boolean` | no | Use the GPT-4 generation path when supported. |
| `suffix` | body | `string` | no | Optional suffix appended to the generated output. |
