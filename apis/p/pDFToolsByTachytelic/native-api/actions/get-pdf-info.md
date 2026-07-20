# Get PDF Info with PDF Tools by Tachytelic

## Endpoint

- **Method:** `POST`
- **Path:** `/getinfo`
- **Base URL:** `https://pdf.tachytelic.net/api`
- **Official documentation:** [Get PDF Info](https://learn.microsoft.com/en-us/connectors/pdftoolsbytachytelic/#extract-info)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PdfFileContent` | body | `string` | yes | Base64-encoded PDF file content. |
