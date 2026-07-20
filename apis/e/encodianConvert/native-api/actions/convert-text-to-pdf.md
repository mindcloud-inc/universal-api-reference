# Convert - Text to PDF with Encodian - Convert

Creates a PDF file from text in Encodian - Convert.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/TextToPDF`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert - Text to PDF](https://support.encodian.com/hc/en-gb/articles/360011683054-Convert-Text-to-PDF)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FileName` | body | `string` | yes | Filename for source text file when file content is provided. |
| `outputFilename` | body | `string` | yes | The filename of the output PDF document. |
| `textData` | body | `string` | no | Text to convert into a PDF document. Provide either text data or file content. |
| `FinalOperation` | body | `boolean` | no | Return the processed file instead of just an Operation ID. |
| `textEncodingType` | body | `string` | no | The encoding type used for text conversion. |
