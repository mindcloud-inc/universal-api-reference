# Merge PDFs with PDF Tools by Tachytelic

## Endpoint

- **Method:** `POST`
- **Path:** `/merge`
- **Base URL:** `https://pdf.tachytelic.net/api`
- **Official documentation:** [Merge PDFs](https://learn.microsoft.com/en-us/connectors/pdftoolsbytachytelic/#merge-pdfs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PdfFiles[]` | body | `array<string>` | yes | Array of base64-encoded PDF files to merge. Send multiple values as a array. |
