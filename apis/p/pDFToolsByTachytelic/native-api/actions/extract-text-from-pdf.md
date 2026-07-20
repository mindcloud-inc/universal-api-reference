# Extract Text from PDF with PDF Tools by Tachytelic

## Endpoint

- **Method:** `POST`
- **Path:** `/extracttext`
- **Base URL:** `https://pdf.tachytelic.net/api`
- **Official documentation:** [Extract Text from PDF](https://learn.microsoft.com/en-us/connectors/pdftoolsbytachytelic/#extract-text)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PdfFileContent` | body | `string` | yes | Base64-encoded PDF file content. |
| `StartPage` | body | `number` | no | Optional page number to start text extraction from. |
| `EndPage` | body | `number` | no | Optional page number to stop text extraction at, inclusive. |
