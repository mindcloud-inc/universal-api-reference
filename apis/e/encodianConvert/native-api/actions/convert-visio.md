# Convert - Visio with Encodian - Convert

Creates a converted file from a Visio document in Encodian - Convert.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/ConvertVisio`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert - Visio](https://support.encodian.com/hc/en-gb/articles/5306216347665)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputFormatParameter` | query | `string` | yes | Set the output file type used by Encodian's dynamic schema. |
| `outputFormat` | body | `string` | yes | Select the output file type format. |
| `fileName` | body | `string` | yes | The filename of the source file, including extension. |
| `fileContent` | body | `file` | yes | The file content of the source file. |
