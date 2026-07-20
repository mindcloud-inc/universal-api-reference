# Convert - CAD with Encodian - Convert

Creates a converted file from a CAD file in Encodian - Convert.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/ConvertCad`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert - CAD](https://support.encodian.com/hc/en-gb/articles/4542607350417)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputFormatParameter` | query | `string` | yes | Set the output file type used by Encodian's dynamic schema. |
| `outputFilename` | body | `string` | yes | The filename of the output document. |
| `fileName` | body | `string` | yes | The filename of the source file, including extension. |
| `fileContent` | body | `file` | yes | The file content of the source CAD file. |
| `outputFormat` | body | `string` | yes | The format of the output file. |
