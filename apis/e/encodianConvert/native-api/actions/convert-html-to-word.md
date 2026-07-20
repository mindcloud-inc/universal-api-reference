# Convert - HTML to Word with Encodian - Convert

Creates a Word file from HTML or a web URL in Encodian - Convert.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/HtmlToWord`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert - HTML to Word](https://support.encodian.com/hc/en-gb/articles/360011823213)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FileName` | body | `string` | yes | The filename of the source HTML file. |
| `outputFilename` | body | `string` | yes | The filename of the output Word document. |
| `FinalOperation` | body | `boolean` | yes | Return the processed file instead of just an Operation ID. |
| `fileContent` | body | `file` | no | HTML file content to convert. |
| `htmlData` | body | `string` | no | Raw HTML content to convert. |
