# Generate AI Answer with Moorcheh

Generates an AI answer in Moorcheh from your data.

## Endpoint

- **Method:** `POST`
- **Path:** `/answer`
- **Base URL:** `https://api.moorcheh.ai/v1`
- **Official documentation:** [Generate AI Answer](https://docs.moorcheh.ai/api-reference/ai/generate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `namespace` | body | `string` | yes | Namespace for search mode, or an empty string for direct AI mode. |
| `query` | body | `string` | yes | Question or prompt to answer. |
| `top_k` | body | `number` | no | Number of relevant chunks to use in search mode. Defaults to 10 in Moorcheh. |
| `threshold` | body | `number` | no | Minimum relevance score from 0 to 1. Required when kiosk mode is enabled. |
| `temperature` | body | `number` | no | AI creativity level from 0.0 to 2.0. Moorcheh defaults to 0.7. |
| `ai_model` | body | `string` | no | Optional Moorcheh AI model ID such as deepseek.r1-v1:0. |
| `kiosk_mode` | body | `boolean` | no | Enable threshold-based filtering for namespace-backed answers. |
| `header_prompt` | body | `string` | no | Optional instruction prepended to the model prompt. |
| `footer_prompt` | body | `string` | no | Optional instruction appended to the prompt. Moorcheh defaults to a concise-answer instruction. |
