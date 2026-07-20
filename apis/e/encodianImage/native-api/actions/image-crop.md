# Image - Crop with Encodian - Image

Creates a cropped image in Encodian - Image.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Image/CropImage`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Image - Crop](https://support.encodian.com/hc/en-gb/articles/10860483459740/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cropType` | body | `list` | yes | Crop method to use, such as borders or rectangle. Accepted values: `Border`, `Rectangle`. |
| `fileContent` | body | `string` | yes | Base64 content of the source image file. |
| `leftBorder` | body | `number` | no | Pixel adjustment for the left border. |
| `rightBorder` | body | `number` | no | Pixel adjustment for the right border. |
| `topBorder` | body | `number` | no | Pixel adjustment for the top border. |
| `bottomBorder` | body | `number` | no | Pixel adjustment for the bottom border. |
| `upperLeftX` | body | `number` | no | Upper-left X coordinate of the crop area in pixels. |
| `upperLeftY` | body | `number` | no | Upper-left Y coordinate of the crop area in pixels. |
| `width` | body | `number` | no | Crop area width in pixels. |
| `height` | body | `number` | no | Crop area height in pixels. |
