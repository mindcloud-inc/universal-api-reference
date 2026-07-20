# Create DOCX Or PDF from DOCX Template URL As Base64 Response with DocMaker

Creates a DOCX or PDF from a template URL as Base64 in DocMaker.

## Endpoint

- **Method:** `POST`
- **Path:** `/docx_fill_convert`
- **Base URL:** `https://api.v2.docmaker.co`
- **Official documentation:** [Create DOCX Or PDF from DOCX Template URL As Base64 Response](https://guide.docmaker.co/features/create-pdf-from-docx-template/docx_fill_convert-api-parameters)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `templateURL` | body | `string` | yes |
| `data` | body | `object` | no |
| `outputType` | body | `string` | yes |
| `metadata` | body | `string` | no |
