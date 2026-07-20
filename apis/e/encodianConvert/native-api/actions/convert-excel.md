# Convert - Excel with Encodian - Convert

Creates a converted file from an Excel document in Encodian - Convert.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/ConvertExcel`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert - Excel](https://support.encodian.com/hc/en-gb/articles/360011804178)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputFormatParameter` | query | `string` | yes | Set the output file type used by Encodian's dynamic schema. |
| `outputFilename` | body | `string` | yes | The filename of the output document. |
| `fileContent` | body | `file` | yes | The file content of the source file. |
| `fileName` | body | `string` | yes | The filename of the source file, including extension. |
| `outputFormat` | body | `string` | yes | Select the output file type format. |
