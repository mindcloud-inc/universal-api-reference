# Enhance Lighting with DeepImage

Creates an image with enhanced lighting in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process_result`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Enhance Lighting](https://documentation.deep-image.ai/image-processing/enhance-lighting-and-colors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the source image whose lighting should be enhanced. |
| `light_parameters.type` | body | `string` | no | Lighting algorithm: hdr_light_advanced, hdr_light, or contrast. |
| `light_parameters.level` | body | `number` | no | Lighting strength from 0.0 to 1.0. |
