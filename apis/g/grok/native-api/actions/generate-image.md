# Generate Image with Grok

Creates images from prompts in Grok.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/images/generations`
- **Base URL:** `https://api.x.ai`
- **Official documentation:** [Generate Image](https://docs.x.ai/developers/rest-api-reference/inference/images#image-generation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | xAI image generation model. |
| `prompt` | body | `string` | yes | Text prompt describing the image to generate. |
| `n` | body | `number` | no | Number of images to generate. |
| `aspect_ratio` | body | `string` | no | Desired output aspect ratio. |
| `resolution` | body | `string` | no | Desired output resolution. |
