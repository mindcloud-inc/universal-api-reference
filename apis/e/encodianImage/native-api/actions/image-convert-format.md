# Image - Convert Format with Encodian - Image

Creates an image in a new format in Encodian - Image.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Image/ImageConvertFormat`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Image - Convert Format](https://support.encodian.com/hc/en-gb/articles/360006617857-Convert-Image-Format)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | Base64 content of the source image file. |
| `newImageFormat` | body | `list` | yes | The target image file format. Accepted values: `BMP`, `GIF`, `JPG`, `PNG`, `TIF`. |
| `fileName` | body | `string` | yes | The filename of the source image file. |
| `currentImageFormat` | body | `list` | yes | The current image file format. Accepted values: `BMP`, `GIF`, `HEIC`, `JPG`, `PNG`, `TIF`. |
