# Optimize PDF with PDF Tools by Tachytelic

## Endpoint

- **Method:** `POST`
- **Path:** `/optimize`
- **Base URL:** `https://pdf.tachytelic.net/api`
- **Official documentation:** [Optimize PDF](https://learn.microsoft.com/en-us/connectors/pdftoolsbytachytelic/#optimize-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PdfFileContent` | body | `string` | yes | Base64-encoded PDF file content to optimize. |
| `Mode` | body | `list` | no | Optimization mode: safe or aggressive. Accepted values: `0`, `1`. |
| `Garbage` | body | `number` | no | Unused object removal level from 0 to 4. |
| `Deflate` | body | `boolean` | no | Whether to apply deflate compression to PDF streams. |
| `Clean` | body | `boolean` | no | Whether to clean and sanitize the PDF content. |
