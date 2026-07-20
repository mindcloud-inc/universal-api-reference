# Convert - PDF to Images with Encodian - Convert

Creates image files from a PDF in Encodian - Convert.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/ConvertPdfToImages`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert - PDF to Images](https://support.encodian.com/hc/en-gb/articles/4418101623441)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `file` | yes | The file content of the source PDF file. |
| `imageFormat` | body | `string` | yes | The format of the output image files. |
| `filenamePrefix` | body | `string` | no | Prefix for generated image files. |
