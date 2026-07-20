# Convert - HTML to PDF with Encodian - Convert

Creates a PDF file from HTML or a web URL in Encodian - Convert.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/HtmlToPDF`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert - HTML to PDF](https://support.encodian.com/hc/en-gb/articles/360022205154-Convert-HTML-to-PDF)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FileName` | body | `string` | yes | The filename of the source HTML file. |
| `outputFilename` | body | `string` | yes | The filename of the output PDF document. |
| `encoding` | body | `string` | yes | The encoding type used for HTML conversion. |
| `htmlData` | body | `string` | no | Raw HTML content to convert. |
| `fileContent` | body | `file` | no | HTML file content to convert. |
| `FinalOperation` | body | `boolean` | no | Whether to return the converted file content immediately. |
