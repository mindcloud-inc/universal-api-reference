# Delete a Tax Line with Veryfi

Deletes a tax line from a document in Veryfi.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v8/partner/documents/:document_id/tax-lines/:tax_line_id`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Delete a Tax Line](https://docs.veryfi.com/api/delete-a-tax-line/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `document_id` | path | `string` | yes |
| `tax_line_id` | path | `string` | yes |
