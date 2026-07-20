# Add Text Watermark with PDF Blocks

Updates a PDF document with a text watermark in PDF Blocks.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/add_watermark/text`
- **Base URL:** `https://api.pdfblocks.com`
- **Official documentation:** [Add Text Watermark](https://www.pdfblocks.com/docs/api/add-text-watermark-to-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The input PDF document. |
| `line_1` | body | `string` | yes | The first line of text of the watermark. |
| `line_2` | body | `string` | no | The second line of text of the watermark. |
| `line_3` | body | `string` | no | The third line of text of the watermark. |
| `template` | body | `number` | no | The text watermark template ID. |
| `color` | body | `string` | no | The color of the text watermark. |
| `transparency` | body | `number` | no | The transparency level for the text watermark. |
| `margin` | body | `number` | no | The distance in inches from the border of the page to the text watermark. |
