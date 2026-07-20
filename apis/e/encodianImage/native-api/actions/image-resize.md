# Image - Resize with Encodian - Image

Creates a resized image in Encodian - Image.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Image/ResizeImage`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Image - Resize](https://support.encodian.com/hc/en-gb/articles/360018591034-Resize-an-Image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FileName` | body | `string` | yes | The filename of the source image file. The file extension is mandatory. |
| `FileContent` | body | `string` | yes | Base64 content of the source image file. |
| `ImageResizeType` | body | `list` | yes | Whether the image should be resized by ratio or by specific dimensions. Accepted values: `Percentage`, `Specific`. |
| `FinalOperation` | body | `boolean` | yes | Return the processed file content instead of only an operation ID. |
| `ResizePercentage` | body | `number` | no | Percentage used for ratio-based resize. |
| `ImageWidth` | body | `number` | no | Target image width in pixels. |
| `ImageHeight` | body | `number` | no | Target image height in pixels. |
| `MaintainAspectRatio` | body | `boolean` | no | Automatically calculate height from width when resizing to dimensions. |
| `ImageResolution` | body | `number` | no | Optional output image resolution. |
