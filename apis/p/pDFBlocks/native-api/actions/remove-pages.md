# Remove Pages with PDF Blocks

Updates a PDF document by removing pages in PDF Blocks.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/remove_pages`
- **Base URL:** `https://api.pdfblocks.com`
- **Official documentation:** [Remove Pages](https://www.pdfblocks.com/docs/api/remove-pages-from-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The input PDF document. |
| `first_page` | body | `number` | no | The first page of the range to remove from the PDF document. |
| `last_page` | body | `number` | no | The last page of the range to remove from the PDF document. |
