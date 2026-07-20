# Add Watermark to PDF with Plumsail Documents

Adds a watermark to a PDF in Plumsail Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/watermark/pdf-to-pdf`
- **Base URL:** `https://us-api.plumsail.com`
- **Official documentation:** [Add Watermark to PDF](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Watermark)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `LayerPosition` | body | `string` | no |
| `StartPage` | body | `number` | no |
| `EndPage` | body | `number` | no |
| `Pages` | body | `string` | no |
| `File` | body | `file` | no |
| `FileUrl` | body | `string` | no |
| `CallbackUrl` | body | `string` | no |
| `OverlayFile` | body | `file` | no |
| `OverlayFileUrl` | body | `string` | no |
