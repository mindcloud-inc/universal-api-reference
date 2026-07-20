# Create PDF from DOCX Template URL with DocMaker

Creates a PDF from a DOCX template URL in DocMaker.

## Endpoint

- **Method:** `POST`
- **Path:** `/docx_fill_convert`
- **Base URL:** `https://api.v2.docmaker.co`
- **Official documentation:** [Create PDF from DOCX Template URL](https://guide.docmaker.co/features/create-pdf-from-docx-template/docx_fill_convert-api-parameters)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `templateURL` | body | `string` | yes |
| `data` | body | `object` | no |
| `metadata` | body | `string` | no |
