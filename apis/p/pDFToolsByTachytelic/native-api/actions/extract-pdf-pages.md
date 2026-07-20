# Extract PDF Pages with PDF Tools by Tachytelic

## Endpoint

- **Method:** `POST`
- **Path:** `/extractpages`
- **Base URL:** `https://pdf.tachytelic.net/api`
- **Official documentation:** [Extract PDF Pages](https://learn.microsoft.com/en-us/connectors/pdftoolsbytachytelic/#extract-specific-pages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PdfFileContent` | body | `string` | yes | Base64-encoded PDF file content. |
| `PageRange` | body | `string` | yes | Page range to extract, for example 1-3,7. |
