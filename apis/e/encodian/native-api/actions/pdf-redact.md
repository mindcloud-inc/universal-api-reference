# PDF Redact with Encodian

Redacts text in a PDF with Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/PDF/RedactPdf`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [PDF Redact](https://support.encodian.com/hc/en-gb/articles/360018607954)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Filename` | body | `string` | yes | The PDF filename including the file extension. |
| `FileContent` | body | `string` | yes | A Base64 encoded representation of the PDF file to be processed. |
| `Redactions[]` | body | `array<object>` | yes | An array of redactions to apply. |
| `FinalOperation` | body | `boolean` | no | Set whether to return the file or just an operation ID. |
