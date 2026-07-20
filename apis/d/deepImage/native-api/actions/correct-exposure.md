# Correct Exposure with DeepImage

Creates an image with corrected exposure in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process_result`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Correct Exposure](https://documentation.deep-image.ai/image-processing/enhance-lighting-and-colors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the source image whose exposure should be corrected. |
