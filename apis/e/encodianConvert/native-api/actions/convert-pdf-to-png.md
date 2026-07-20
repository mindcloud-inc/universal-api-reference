# Convert - PDF to PNG with Encodian - Convert

Creates a PNG file from a PDF in Encodian - Convert.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/ConvertPdfToPng`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert - PDF to PNG](https://support.encodian.com/hc/en-gb/articles/10086003836701)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `file` | yes | The file content of the source PDF file. |
| `bitDepth` | body | `number` | yes | PDF bit depth for generated PNG output. |
| `outputFilename` | body | `string` | no | Output image filename. |
