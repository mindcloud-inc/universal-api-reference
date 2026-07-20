# Create Agent Response with Perplexity

Creates an agent response in Perplexity.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/agent`
- **Base URL:** `https://api.perplexity.ai`
- **Official documentation:** [Create Agent Response](https://docs.perplexity.ai/api-reference/responses-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | Input content. Perplexity also accepts array-form input items; this action currently models the common string input path. |
| `instructions` | body | `string` | no | System instructions for the model. |
| `model` | body | `string` | no | Model ID in provider/model format. |
| `preset` | body | `string` | no | Preset configuration name such as fast-search or pro-search. |
| `max_output_tokens` | body | `number` | no | Maximum tokens to generate. |
| `max_steps` | body | `number` | no | Maximum research loop steps. |
| `stream` | body | `boolean` | no | When true, returns SSE events instead of JSON. |
| `language_preference` | body | `string` | no | ISO 639-1 language code for the preferred response language. |
