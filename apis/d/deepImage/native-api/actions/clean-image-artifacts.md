# Clean Image Artifacts with DeepImage

Creates an artifact-cleaned image in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process_result`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Clean Image Artifacts](https://documentation.deep-image.ai/image-processing/denoise-and-sharpen)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the source image to clean. |
