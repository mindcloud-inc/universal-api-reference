# Create PDF Link from URL with PDFBolt

Creates a PDF download link from a URL in PDFBolt.

## Endpoint

- **Method:** `POST`
- **Path:** `/sync`
- **Base URL:** `https://api.pdfbolt.com/v1`
- **Official documentation:** [Create PDF Link from URL](https://pdfbolt.com/docs/api-endpoints/sync)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL to convert into a PDF link. |
