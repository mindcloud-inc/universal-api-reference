# Merge PDFs with PDF-app

Creates a merged PDF in PDF-app.

## Endpoint

- **Method:** `POST`
- **Path:** `/merge_pdf`
- **Base URL:** `https://api.pdf-app.net`
- **Official documentation:** [Merge PDFs](https://pdf-app.net/apidocumentation?type=merge_pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pdfUrls[]` | body | `array<string>` | yes | Public URLs of the PDF files to merge in order. |
| `async` | body | `boolean` | no | Set true to queue the merge asynchronously. |
| `fileName` | body | `string` | no | Optional output file name for the merged PDF. |
