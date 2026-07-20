# Extract Pages with PDF Blocks

Creates a PDF document with extracted pages in PDF Blocks.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/extract_pages`
- **Base URL:** `https://api.pdfblocks.com`
- **Official documentation:** [Extract Pages](https://www.pdfblocks.com/docs/api/extract-pages-from-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The input PDF document. |
| `first_page` | body | `number` | no | The first page of the range to extract. |
| `last_page` | body | `number` | no | The last page of the range to extract. |
