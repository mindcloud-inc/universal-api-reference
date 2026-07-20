# Convert - Email with Encodian - Convert

Creates a PDF file from an email and attachments in Encodian - Convert.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/ConvertMailMessage`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert - Email](https://support.encodian.com/hc/en-gb/articles/360011566298-Convert-Email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputFilename` | body | `string` | yes | The filename of the output PDF document. |
| `fileName` | body | `string` | yes | The filename of the source MSG or EML file. |
| `fileContent` | body | `file` | yes | The file content of the source email file. |
