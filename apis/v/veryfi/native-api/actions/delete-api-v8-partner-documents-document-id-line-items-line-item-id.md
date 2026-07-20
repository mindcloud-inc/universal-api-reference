# Delete a Line Item with Veryfi

Deletes a line item from a document in Veryfi.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v8/partner/documents/:document_id/line-items/:line_item_id`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Delete a Line Item](https://docs.veryfi.com/api/receipts-invoices/delete-a-line-item/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `document_id` | path | `string` | yes |
| `line_item_id` | path | `string` | yes |
