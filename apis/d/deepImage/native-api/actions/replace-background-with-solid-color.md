# Replace Background with Solid Color with DeepImage

Creates an image with a solid-color background in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process_result`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Replace Background with Solid Color](https://documentation.deep-image.ai/image-processing/background-removal-and-generation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the source image whose background should be replaced with a solid color. |
| `background.color` | body | `string` | no | Solid background color, such as #FFFFFF or transparent. |
