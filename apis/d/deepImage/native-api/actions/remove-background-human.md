# Remove Background (Human) with DeepImage

Creates an image with human background removal in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process_result`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Remove Background (Human)](https://documentation.deep-image.ai/image-processing/background-removal-and-generation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the source image whose human background should be removed. |
