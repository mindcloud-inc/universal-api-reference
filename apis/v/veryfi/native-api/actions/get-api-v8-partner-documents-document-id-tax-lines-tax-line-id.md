# Returns document Tax Line with Veryfi

Retrieves a tax line from a document in Veryfi.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v8/partner/documents/:document_id/tax-lines/:tax_line_id`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Returns document Tax Line](https://docs.veryfi.com/api/returns-document-tax-line/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `document_id` | path | `string` | yes |
| `tax_line_id` | path | `string` | yes |
