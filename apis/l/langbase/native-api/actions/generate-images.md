# Generate Images with Langbase

## Endpoint

- **Method:** `POST`
- **Path:** `v1/images`
- **Base URL:** `https://api.langbase.com`
- **Official documentation:** [Generate Images](https://langbase.com/docs/api-reference/images)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Prompt describing the image to generate. |
| `model` | body | `string` | yes | Image model identifier, for example `openai:dall-e-3` or `google:imagen-3.0-generate-002`. |
| `llmApiKey` | body | `string` | no | Provider model API key for the `LB-LLM-Key` request header when the selected image model is not already configured in Langbase. |
