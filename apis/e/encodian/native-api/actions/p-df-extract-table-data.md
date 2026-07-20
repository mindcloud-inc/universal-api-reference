# PDF Extract Table Data with Encodian

Extracts PDF table data in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/PDF/PdfExtractTableData`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [PDF Extract Table Data](https://support.encodian.com/hc/en-gb/articles/15064945594268)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | A Base64 encoded representation of the PDF file to be processed. |
| `extract` | body | `string` | yes | Specify the table to extract. |
| `startPage` | body | `number` | no | Specifies the page number to start extracting tables from. |
| `endPage` | body | `number` | no | Specifies the page number to stop extracting tables on. |
| `tableIndex` | body | `number` | no | If Extract is set to Custom, specify the index of the table to extract. |
| `hasHeaderRow` | body | `boolean` | no | Set whether the first row is a header row. |
