# Edit Image With Flux Kontext Max Image To Image with AI/ML API

Creates an edited image with Flux Kontext Max in AI/ML API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/images/generations`
- **Base URL:** `https://api.aimlapi.com`
- **Official documentation:** [Edit Image With Flux Kontext Max Image To Image](https://docs.aimlapi.com/api-references/image-models/flux/flux-kontext-max-image-to-image)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `aspect_ratio` | body | `string` | no |
| `guidance_scale` | body | `number` | no |
| `image_url` | body | `string` | yes |
| `num_images` | body | `number` | no |
| `prompt` | body | `string` | yes |
