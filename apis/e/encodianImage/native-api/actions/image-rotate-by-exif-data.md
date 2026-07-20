# Image - Rotate by EXIF Data with Encodian - Image

Creates a JPG rotated by EXIF data in Encodian - Image.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Image/RotateImageByExifData`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Image - Rotate by EXIF Data](https://support.encodian.com/hc/en-gb/articles/16556447851804)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | Base64 content of a source JPG file that contains an EXIF orientation tag. |
