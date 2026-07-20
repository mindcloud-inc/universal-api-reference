# Convert - PDF to JPG with Encodian - Convert

Creates a JPG file from a PDF in Encodian - Convert.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/ConvertPdfToJpg`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert - PDF to JPG](https://support.encodian.com/hc/en-gb/articles/11096881397277)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `file` | yes | The file content of the source PDF file. |
| `outputFilename` | body | `string` | no | Output image filename. |
