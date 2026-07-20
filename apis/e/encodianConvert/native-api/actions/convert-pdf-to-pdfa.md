# Convert - PDF to PDFA with Encodian - Convert

Creates a PDF/A file from a PDF in Encodian - Convert.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/ConvertToPdfA`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert - PDF to PDFA](https://support.encodian.com/hc/en-gb/articles/360010578413)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FileName` | body | `string` | yes | The filename of the source PDF file, including extension. |
| `fileContent` | body | `file` | no | PDF file content to convert. |
| `pdfaComplianceLevel` | body | `string` | no | Target PDF/A compliance level. |
| `FinalOperation` | body | `boolean` | no | Whether to return the converted file content immediately. |
