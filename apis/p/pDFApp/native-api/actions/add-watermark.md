# Add Watermark with PDF-app

Updates a PDF with a watermark in PDF-app.

## Endpoint

- **Method:** `POST`
- **Path:** `/waterMark`
- **Base URL:** `https://api.pdf-app.net`
- **Official documentation:** [Add Watermark](https://pdf-app.net/apidocumentation?type=waterMark)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileUrl` | body | `string` | yes | File URL to watermark. |
| `fileName` | body | `string` | no | Desired output file name. |
| `fontType` | body | `string` | no | PDF text watermark font type. |
| `customFont` | body | `string` | no | Custom font download URL for text watermarks. |
| `watermarkText` | body | `string` | no | Text to use as the watermark. |
| `textColor` | body | `string` | no | Hex color for the text watermark. |
| `textOpacity` | body | `number` | no | Opacity for the text watermark. |
| `fontSize` | body | `number` | no | Font size for the text watermark. |
| `placement` | body | `string` | no | Placement preset for the watermark. |
| `textAngle` | body | `number` | no | Rotation angle for the text watermark. |
| `horizontal_margine` | body | `number` | no | Horizontal offset for the watermark. |
| `vertical_margine` | body | `number` | no | Vertical offset for the watermark. |
| `pageRange` | body | `string` | no | Page range to apply the watermark to. |
| `watermarkImageUrl` | body | `string` | no | Optional image URL to use as the watermark. |
| `imageAngle` | body | `number` | no | Rotation angle for the image watermark. |
| `imageScale` | body | `number` | no | Scale factor for the image watermark. |
| `imageOpacity` | body | `number` | no | Opacity for the image watermark. |
| `fixedWidth` | body | `number` | no | Fixed width for the image watermark. |
