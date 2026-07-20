# Image - Compress with Encodian - Image

Creates a compressed image in Encodian - Image.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Image/CompressImage`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Image - Compress](https://support.encodian.com/hc/en-gb/articles/360027350513-Compress-an-Image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | Base64 content of the source image file. |
| `fileName` | body | `string` | yes | The filename of the source image file. |
| `imageType` | body | `list` | yes | The source image file format. Accepted values: `JPG`, `PNG`. |
