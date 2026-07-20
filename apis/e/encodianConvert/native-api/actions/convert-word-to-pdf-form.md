# Convert - Word to PDF Form with Encodian - Convert

Creates a PDF form from a Word document in Encodian - Convert.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/WordToPdfForm`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert - Word to PDF Form](https://support.encodian.com/hc/en-gb/articles/360012307133)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FileName` | body | `string` | yes | The filename of the source Microsoft Word file. |
| `fileContent` | body | `file` | yes | The file content of the source Microsoft Word file. |
| `outputFilename` | body | `string` | yes | The filename of the output PDF document. |
