# Image - Remove EXIF Tags with Encodian - Image

Creates an image without EXIF tags in Encodian - Image.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Image/ImageRemoveExifTags`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Image - Remove EXIF Tags](https://support.encodian.com/hc/en-gb/articles/4415700524817)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | Base64 content of the source image file. |
| `fileName` | body | `string` | yes | The filename of the source image file. |
| `imageType` | body | `list` | yes | Source image format. Runtime verification showed this endpoint accepts JPG, JPEG, TIF, or TIFF; PNG is rejected by the provider for EXIF removal. Accepted values: `JPEG`, `JPG`, `TIF`, `TIFF`. |
