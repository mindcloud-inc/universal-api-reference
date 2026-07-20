# Transfer Image Style with Picsart

Creates an image with transferred style in Picsart.

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/1.0/styletransfer`
- **Base URL:** `https://api.picsart.io`
- **Official documentation:** [Transfer Image Style](https://docs.picsart.io/reference/image-transfer-style)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image_url` | body | `string` | yes | Source image URL. |
| `reference_image_url` | body | `string` | yes | Reference image URL to transfer style from. |
| `level` | body | `string` | no | Choose one of the supported style intensity levels. |
| `format` | body | `string` | no | Optional output image format. |
