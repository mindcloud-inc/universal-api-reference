# Create PDF from URL with PDFBolt

Creates a PDF from a URL in PDFBolt.

## Endpoint

- **Method:** `POST`
- **Path:** `/direct`
- **Base URL:** `https://api.pdfbolt.com/v1`
- **Official documentation:** [Create PDF from URL](https://pdfbolt.com/docs/api-endpoints/direct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL to convert into a PDF. |
