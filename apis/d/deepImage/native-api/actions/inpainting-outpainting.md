# Inpainting / Outpainting with DeepImage

Creates an inpainted or outpainted image in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Inpainting / Outpainting](https://documentation.deep-image.ai/image-processing/inpainting-and-outpainting-uncrop)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the source image to edit or expand. |
| `background.generate.adapter_type` | body | `string` | no | Use `inpainting` for masked edits or `upscale` when pairing prompt guidance with outpainting. |
| `background.generate.description` | body | `string` | no | Prompt for the fill or uncrop result. |
| `background.generate.ip_image2` | body | `string` | no | Public URL of the mask image used for inpainting. |
| `background.generate.controlnet_conditioning_scale` | body | `number` | no | DeepImage conditioning scale for inpainting masks. |
| `width` | body | `number` | no | Target width used for uncrop/outpainting workflows. |
| `height` | body | `number` | no | Target height used for uncrop/outpainting workflows. |
| `fit.canvas` | body | `string` | no | Canvas expansion mode used for outpainting. |
