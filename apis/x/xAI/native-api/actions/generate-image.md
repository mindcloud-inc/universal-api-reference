# Generate Image with xAI

Creates an image in the xAI API.

## Endpoint

- **Method:** `POST`
- **Path:** `/images/generations`
- **Base URL:** `https://api.x.ai/v1`
- **Official documentation:** [Generate Image](https://docs.x.ai/developers/rest-api-reference/inference/images#image-generation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | no | Image generation model name. |
| `prompt` | body | `string` | no | Prompt for image generation. |
