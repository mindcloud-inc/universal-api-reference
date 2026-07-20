# Image - Add Image Watermark with Encodian - Image

Creates an image with an image watermark in Encodian - Image.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Image/AddImageWatermarkToImage`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Image - Add Image Watermark](https://support.encodian.com/hc/en-gb/articles/8967068141597)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | body | `string` | yes | The filename of the source file. The file extension is mandatory, such as file.png. |
| `fileContent` | body | `string` | yes | Base64 content of the source image file. |
| `watermarkFilename` | body | `string` | yes | The filename of the watermark image file. The file extension is mandatory. |
| `watermarkFileContent` | body | `string` | yes | Base64 content of the watermark image file. |
| `watermarkPosition` | body | `list` | yes | The position of the image watermark on the source image. Accepted values: `BottomLeft`, `BottomRight`, `CentreHorizontal`, `CentreVertical`, `Custom`, `Diagonal`, `TopLeft`, `TopRight`. |
| `imageYOffSet` | body | `number` | no | Vertical watermark offset in pixels when Watermark Position is Custom. |
| `imageXOffset` | body | `number` | no | Horizontal watermark offset in pixels when Watermark Position is Custom. |
| `rotationAngle` | body | `number` | no | Rotation angle for the watermark image in degrees. |
| `opacity` | body | `number` | no | Watermark opacity from 0.0 to 1.0. Default is 0.7. |
| `alignImage` | body | `boolean` | no | Align the source image using EXIF orientation tags. |
| `alignWatermark` | body | `boolean` | no | Align the watermark image using EXIF orientation tags. |
