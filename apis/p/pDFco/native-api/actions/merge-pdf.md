# Merge PDF with PDF.co

Creates a merged PDF in PDF.co.

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf/merge`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [Merge PDF](https://docs.pdf.co/api-reference/merge/pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Comma-separated list of PDF URLs to merge. |
| `name` | body | `string` | no | Optional output filename. |
| `async` | body | `boolean` | no | Process merge as background job. |
| `profiles` | body | `string` | no | Optional profiles JSON string for advanced merge settings. |
