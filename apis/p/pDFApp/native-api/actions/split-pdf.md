# Split PDF with PDF-app

Creates split PDF files in PDF-app.

## Endpoint

- **Method:** `POST`
- **Path:** `/splitt_PDF`
- **Base URL:** `https://api.pdf-app.net`
- **Official documentation:** [Split PDF](https://pdf-app.net/apidocumentation?type=splitt_PDF)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileUrl` | body | `string` | yes | Public URL of the PDF to split. |
| `pagesPerSplit` | body | `number` | yes | Number of pages to include in each split PDF. |
| `pageRanges` | body | `string` | no | Optional custom page ranges to split, such as 1-2,4-5. |
| `async` | body | `boolean` | no | Set true to run the split asynchronously. |
| `fileName` | body | `string` | no | Optional base file name for the split outputs. |
