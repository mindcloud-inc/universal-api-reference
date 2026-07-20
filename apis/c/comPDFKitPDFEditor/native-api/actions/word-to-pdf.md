# Word to PDF with ComPDFKit PDF Editor

Creates a Word-to-PDF conversion task in ComPDFKit PDF Editor.

## Endpoint

- **Method:** `POST`
- **Path:** `/server/v2/process/docx/pdf`
- **Base URL:** `https://api-server.compdf.com`
- **Official documentation:** [Word to PDF](https://api.compdf.com/api-reference/conversion-guides)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
