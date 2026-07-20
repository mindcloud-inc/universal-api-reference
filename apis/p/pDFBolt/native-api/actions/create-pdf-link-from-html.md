# Create PDF Link from HTML with PDFBolt

Creates a PDF download link from HTML in PDFBolt.

## Endpoint

- **Method:** `POST`
- **Path:** `/sync`
- **Base URL:** `https://api.pdfbolt.com/v1`
- **Official documentation:** [Create PDF Link from HTML](https://pdfbolt.com/docs/api-endpoints/sync)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html` | body | `string` | yes | Base64-encoded HTML content to convert into a PDF link. |
