# Smart Content Crop with DeepImage

Creates a smart-cropped image in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process_result`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Smart Content Crop](https://documentation.deep-image.ai/image-processing/frame-identification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the source image to content crop. |
| `width` | body | `number` | yes | Target output width in pixels. |
| `height` | body | `number` | yes | Target output height in pixels. |
