# Edit Image With Flux Dev Image To Image with AI/ML API

Creates an edited image with Flux Dev in AI/ML API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/images/generations`
- **Base URL:** `https://api.aimlapi.com`
- **Official documentation:** [Edit Image With Flux Dev Image To Image](https://docs.aimlapi.com/api-references/image-models/flux/flux-dev-image-to-image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guidance_scale` | body | `number` | no | — |
| `image_url` | body | `string` | yes | The URL of the reference image. |
| `num_images` | body | `number` | no | — |
| `prompt` | body | `string` | yes | The text prompt describing how the image should be edited. |
| `strength` | body | `number` | no | — |
