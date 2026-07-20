# Transfer Image Colors with Picsart

Creates an image with transferred colors in Picsart.

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/1.0/color-transfer`
- **Base URL:** `https://api.picsart.io`
- **Official documentation:** [Transfer Image Colors](https://docs.picsart.io/reference/image-transfer-color)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image_url` | body | `string` | yes | Source image URL. |
| `reference_image_url` | body | `string` | yes | Reference image URL to copy colors from. |
| `format` | body | `string` | no | Optional output image format. |
