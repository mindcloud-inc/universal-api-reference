# Add Caption Overlay with DeepImage

Creates an image with caption overlay in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process_result`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Add Caption Overlay](https://documentation.deep-image.ai/image-processing/captions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the source image to caption. |
| `caption.url` | body | `string` | yes | Public URL of the overlay image to place on top of the result. |
| `caption.position` | body | `string` | no | Caption position such as RB, LT, or MM. |
| `caption.target_width_percentage` | body | `number` | no | Caption width as a percentage of the destination image width. |
| `caption.padding` | body | `number` | no | Padding in pixels between the caption and the image border. |
| `caption.opacity` | body | `number` | no | Caption opacity from 0 to 100. |
