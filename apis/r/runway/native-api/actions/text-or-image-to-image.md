# Text Or Image To Image with Runway

Creates an image generation task from text or images in Runway.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/text_to_image`
- **Base URL:** `https://api.dev.runwayml.com`
- **Official documentation:** [Text Or Image To Image](https://docs.dev.runwayml.com/api#tag/Start-generating/paths/~1v1~1text_to_image/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | Image generation model, such as gen4_image_turbo, gen4_image, or gemini_2.5_flash. |
| `promptText` | body | `string` | yes | Detailed text prompt for the image generation. |
| `ratio` | body | `string` | yes | Requested output image ratio, such as 1024:1024 or 1280:720. |
| `referenceImages[]` | body | `array<object>` | yes | One to three reference image objects with uri and optional tag. |
