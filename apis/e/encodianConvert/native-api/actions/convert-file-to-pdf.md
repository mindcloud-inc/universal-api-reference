# Convert - File to PDF with Encodian - Convert

Creates a PDF file from another file in Encodian - Convert.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/BasicConversion`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert - File to PDF](https://support.encodian.com/hc/en-gb/articles/360011123574-Convert-File-to-PDF)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FileName` | body | `string` | yes | The filename of the source file, including extension. |
| `fileContent` | body | `file` | yes | Base64-encoded file content of the source file. |
| `outputFilename` | body | `string` | yes | The filename of the output PDF document. |
| `FinalOperation` | body | `boolean` | no | Whether to return the converted file content immediately. |
