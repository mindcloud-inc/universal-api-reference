# Create Response with OpenRouter

Creates a model response in OpenRouter.

## Endpoint

- **Method:** `POST`
- **Path:** `/responses`
- **Base URL:** `https://openrouter.ai/api/v1/`
- **Official documentation:** [Create Response](https://openrouter.ai/docs/api/api-reference/responses/create-responses)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `model` | body | `string` | yes |
| `input` | body | `string` | yes |
| `instructions` | body | `string` | no |
| `temperature` | body | `number` | no |
| `max_output_tokens` | body | `number` | no |
| `stream` | body | `boolean` | no |
