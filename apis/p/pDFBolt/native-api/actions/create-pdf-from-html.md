# Create PDF from HTML with PDFBolt

Creates a PDF from HTML in PDFBolt.

## Endpoint

- **Method:** `POST`
- **Path:** `/direct`
- **Base URL:** `https://api.pdfbolt.com/v1`
- **Official documentation:** [Create PDF from HTML](https://pdfbolt.com/docs/api-endpoints/direct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html` | body | `string` | yes | Base64-encoded HTML content to convert into a PDF. |
