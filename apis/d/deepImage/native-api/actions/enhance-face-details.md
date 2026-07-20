# Enhance Face Details with DeepImage

Creates an image with enhanced face details in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process_result`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Enhance Face Details](https://documentation.deep-image.ai/image-processing/enhance-face-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the source image whose faces should be enhanced. |
| `face_enhance_parameters.type` | body | `string` | no | Face enhancement model. Use beautify-real or beautify. |
| `face_enhance_parameters.level` | body | `number` | no | Face enhancement level from 0.0 to 1.0. |
| `face_enhance_parameters.smoothing_level` | body | `number` | no | Additional skin smoothing level from 0.0 to 1.0. |
