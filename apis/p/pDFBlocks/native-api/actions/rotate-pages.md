# Rotate Pages with PDF Blocks

Updates a PDF document by rotating pages in PDF Blocks.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/rotate_pages`
- **Base URL:** `https://api.pdfblocks.com`
- **Official documentation:** [Rotate Pages](https://www.pdfblocks.com/docs/api/rotate-pages-in-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The input PDF document. |
| `angle` | body | `number` | yes | The angle of rotation of the pages. |
| `first_page` | body | `number` | no | The first page of the range to rotate in the PDF document. |
| `last_page` | body | `number` | no | The last page of the range to rotate in the PDF document. |
