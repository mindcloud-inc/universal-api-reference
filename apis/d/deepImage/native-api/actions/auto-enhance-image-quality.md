# Auto Enhance Image Quality with DeepImage

Creates an auto-enhanced image in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process_result`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Auto Enhance Image Quality](https://documentation.deep-image.ai/common-usecases/auto-enhance-image-quality)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the source image to auto enhance. |
| `preset` | body | `string` | no | Auto enhance preset. Use auto_enhance, auto_enhance_pro, auto_enhance_qwen, auto_enhance_klein9b, or auto_enhance_generative. |
