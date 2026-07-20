# Image - Add Text Watermark with Encodian - Image

Creates an image with a text watermark in Encodian - Image.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Image/AddTextWatermarkToImage`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Image - Add Text Watermark](https://support.encodian.com/hc/en-gb/articles/360013560398-Add-Text-Watermark-To-Image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FileName` | body | `string` | yes | The filename of the source image file. The file extension is mandatory. |
| `FileContent` | body | `string` | no | Base64 content of the source image file. |
| `Text` | body | `string` | yes | The text to embed as a watermark within the image. |
| `FinalOperation` | body | `boolean` | yes | Return the processed file content instead of only an operation ID. |
| `WatermarkPosition` | body | `list` | no | Position of the text watermark within the image. Accepted values: `BottomLeft`, `BottomRight`, `CentreHorizontal`, `CentreVertical`, `Diagonal`, `TopLeft`, `TopRight`. |
| `Font` | body | `string` | no | Font applied to the text watermark. Default is Arial. |
| `TextColour` | body | `string` | no | HTML colour for the text watermark. Default is #E81123. |
| `TextSize` | body | `number` | no | Font size for the text watermark. Default is 10. |
| `operationId` | body | `string` | no | Advanced: use a previous Encodian operation ID instead of file content. |
