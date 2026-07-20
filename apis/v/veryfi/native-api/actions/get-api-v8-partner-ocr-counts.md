# Get ocr-counts with Veryfi

Retrieves OCR counts from Veryfi.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v8/partner/ocr-counts`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Get ocr-counts](https://docs.veryfi.com/api/get-ocr-counts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ocr_type` | query | `string<string>` | no | Possible values: [ pepsico_codes , pepsico_caps ] Default value: pepsico_codes OCR type |
| `created_date__gt` | query | `string` | no | Created date filter greater than. |
| `created_date__lt` | query | `string` | no | Created date filter lower than. |
| `created_date__gte` | query | `string` | no | Created date filter greater or equal. |
| `created_date__lte` | query | `string` | no | Created date filter lower or equal. |
