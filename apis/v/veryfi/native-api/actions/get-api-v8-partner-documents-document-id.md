# Get a Document with Veryfi

Retrieves a document from Veryfi.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v8/partner/documents/:document_id`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Get a Document](https://docs.veryfi.com/api/receipts-invoices/get-a-document/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | — |
| `bounding_boxes` | query | `boolean` | no | A field used to determine whether or not to return bounding_box and bounding_region for extracted fields in the Document response. |
| `confidence_details` | query | `boolean` | no | A field used to determine whether or not to return the score and ocr_score fields in the Document response. |
| `detailed` | query | `boolean` | no | This field was deprecated on 2023-08-20. Use bounding_boxes and confidence_details . |
| `return_audit_trail` | query | `boolean` | no | Deprecated. |
