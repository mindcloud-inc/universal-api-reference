# Convert - PDF to TIFF with Encodian - Convert

Creates a TIFF file from a PDF in Encodian - Convert.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/ConvertPdfToTiff`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert - PDF to TIFF](https://support.encodian.com/hc/en-gb/articles/4418024925457)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `file` | yes | The file content of the source PDF file. |
| `outputFilename` | body | `string` | no | Output TIFF filename. |
