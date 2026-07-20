# Replace Background with Backdrop Image with DeepImage

Creates an image with a backdrop background in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process_result`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Replace Background with Backdrop Image](https://documentation.deep-image.ai/image-processing/background-removal-and-generation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the source image whose background should be replaced with a backdrop image. |
| `background.replace` | body | `string` | yes | Public URL of the image to use as the replacement background. |
