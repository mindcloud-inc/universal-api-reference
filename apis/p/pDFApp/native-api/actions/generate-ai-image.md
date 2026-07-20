# Generate AI Image with PDF-app

Creates an AI-generated image in PDF-app.

## Endpoint

- **Method:** `POST`
- **Path:** `/ai_img_generator`
- **Base URL:** `https://api.pdf-app.net`
- **Official documentation:** [Generate AI Image](https://pdf-app.net/apidocumentation?type=ai_img_generator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | no | Natural-language prompt describing the image to generate. |
| `fileUrls[]` | body | `array<string>` | no | Optional conditioning image URLs to guide generation. |
| `numberOfImages` | body | `number` | no | How many output images to generate. |
| `width` | body | `number` | no | Output image width in pixels. |
| `height` | body | `number` | no | Output image height in pixels. |
| `cfgScale` | body | `number` | no | Guidance scale controlling prompt adherence versus creativity. |
| `seed` | body | `number` | no | Seed used for reproducible image generation. |
| `quality` | body | `string` | no | Generation quality level: standard or premium. |
| `async` | body | `boolean` | no | Whether to run the image generation asynchronously. |
