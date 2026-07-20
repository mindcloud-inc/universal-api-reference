# Enhance Colors with DeepImage

Creates an image with enhanced colors in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process_result`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Enhance Colors](https://documentation.deep-image.ai/image-processing/enhance-lighting-and-colors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the source image whose colors should be enhanced. |
| `color_parameters.type` | body | `string` | no | Color algorithm: hdr_light_advanced, hdr_light, or contrast. |
| `color_parameters.level` | body | `number` | no | Color strength from 0.0 to 1.0. |
