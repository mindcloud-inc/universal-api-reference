# Generate Image With Gemini 2.5 Flash Image with AI/ML API

Generates an image with Gemini 2.5 Flash Image in AI/ML API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/images/generations`
- **Base URL:** `https://api.aimlapi.com`
- **Official documentation:** [Generate Image With Gemini 2.5 Flash Image](https://docs.aimlapi.com/api-references/image-models/google/gemini-2.5-flash-image)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `aspect_ratio` | body | `string` | no |
| `num_images` | body | `number` | no |
| `prompt` | body | `string` | yes |
