# Perform OCR with Nutrient Document Web Services

Creates a searchable document with OCR in Nutrient Document Web Services API.

## Endpoint

- **Method:** `POST`
- **Path:** `/processor/ocr`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Perform OCR](https://www.nutrient.io/api/reference/public/#tag/Document-Editing/operation/processor-ocr)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | no | Public PDF URL to OCR. |
| `file` | body | `file` | no | PDF file to OCR. |
| `language` | body | `string` | no | OCR language code. |
| `data` | body | `object` | no | Multipart request metadata. |
