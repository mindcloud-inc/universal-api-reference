# Analyze Image with APImage

Extracts text from an image with APImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/ai-image-to-text`
- **Base URL:** `https://apimage.org/api`
- **Official documentation:** [Analyze Image](https://support.apimage.org/article/18-how-to-use-the-ai-image-analyzer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image_url` | body | `string` | yes | URL of the image to analyze. |
| `prompt` | body | `string` | yes | Instruction for what to extract or describe from the image. |
