# Create a Line Item with Veryfi

Creates a line item in a document in Veryfi.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v8/partner/documents/:document_id/line-items`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Create a Line Item](https://docs.veryfi.com/api/receipts-invoices/create-a-line-item/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | — |
| `value` | body | `string` | yes | The category is taken from the line item with the same SKU and/or description. Otherwise from the root category field. string Possible values: >= 4 characters The value to update |
| `bounding_region[]` | body | `array<number>` | yes | The date found on the document and associated with the line item in ISO 8601 format . string Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `order` | body | `number` | no | — |
| `expanded_description` | body | `string` | no | Line item extra product info Possible values: non-empty Possible values: non-empty Possible values: non-empty |
| `tags[]` | body | `array<string>` | no | Possible values: non-empty A user-defined list of identifiers that help to categorize or flag particular types of line items. |
