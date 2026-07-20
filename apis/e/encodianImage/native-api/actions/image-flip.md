# Image - Flip with Encodian - Image

Creates a flipped image in Encodian - Image.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Image/FlipImage`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Image - Flip](https://support.encodian.com/hc/en-gb/articles/9798473339292)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | Base64 content of the source image file. |
| `flipOrientation` | body | `list` | yes | Orientation to flip the image. Accepted values: `Horizontal`, `HorizontalAndVertical`, `Vertical`. |
