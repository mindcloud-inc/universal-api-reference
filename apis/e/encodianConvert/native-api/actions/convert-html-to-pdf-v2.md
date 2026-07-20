# Convert - HTML to PDF (V2) with Encodian - Convert

Creates a PDF file from HTML or a web URL in Encodian - Convert.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/HtmlToPDFV2`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert - HTML to PDF (V2)](https://support.encodian.com/hc/en-gb/articles/16421778005020)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `htmlData` | body | `string` | no | Raw HTML content to convert. |
| `fileContent` | body | `file` | no | HTML file content to convert. |
| `Url` | body | `string` | no | Web page URL to convert. |
| `pageOrientation` | body | `string` | no | PDF page orientation. |
| `pageSize` | body | `string` | no | PDF page size. |
