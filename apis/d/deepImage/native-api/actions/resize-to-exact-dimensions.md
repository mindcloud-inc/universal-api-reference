# Resize to Exact Dimensions with DeepImage

Creates a resized image to exact dimensions in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process_result`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Resize to Exact Dimensions](https://documentation.deep-image.ai/image-processing/resize-and-padding)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the source image to resize. |
| `width` | body | `number` | yes | Exact output width in pixels. |
| `height` | body | `number` | yes | Exact output height in pixels. |
