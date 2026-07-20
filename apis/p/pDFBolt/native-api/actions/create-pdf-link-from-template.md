# Create PDF Link from Template with PDFBolt

Creates a PDF download link from a template in PDFBolt.

## Endpoint

- **Method:** `POST`
- **Path:** `/sync`
- **Base URL:** `https://api.pdfbolt.com/v1`
- **Official documentation:** [Create PDF Link from Template](https://pdfbolt.com/docs/api-endpoints/sync)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateData` | body | `object` | yes | JSON object used to fill the selected template. Use `{}` for blank templates with no variables. |
| `templateId` | body | `string` | yes | ID of the saved PDFBolt template to render. |
