# Search Documents with Veryfi

Finds documents in Veryfi.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v8/partner/documents`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Search Documents](https://docs.veryfi.com/api/receipts-invoices/search-documents/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Default value: 1 The page number. The response is capped to maximum of 50 results per page. |
| `page_size` | query | `number` | no | Default value: 50 The number of Documents per page. |
| `bounding_boxes` | query | `boolean` | no | A field used to determine whether or not to return bounding_box and bounding_region for extracted fields in the Document response. |
| `confidence_details` | query | `boolean` | no | A field used to determine whether or not to return the score and ocr_score fields in the Document response. |
| `detailed` | query | `boolean` | no | This field was deprecated on 2023-08-20. Use bounding_boxes and confidence_details . |
| `q` | query | `string` | no | Case sensitive. Return documents with this text or any extracted fields matching the value exactly. Also matches external_id , notes . Use asterisk for partial matches, e.g. q=Walmart* will return documents with either Walmart in ocr text, any extracted field containing Walmart, or external_id or notes containing Walmart. |
| `order_by` | query | `string` | no | Default value: -created A field used to determine how to order the Documents in the response. For example, the value -created orders by created date with the most recent processed document at the top of the response. |
| `external_id` | query | `string` | no | A custom identification value. Use this if you would like to assign your own ID to documents. This parameter is useful when mapping this document to a service or resource outside Veryfi. |
| `device_id` | query | `string` | no | — |
| `device_user_uuid` | query | `string` | no | — |
| `status` | query | `string` | no | The value indicating the document's status. |
| `tag` | query | `string` | no | An identifier used to help categorize or flag particular types of documents. Use this field to only return Documents with a specific tag. The Document object can have multiple tags. You can create tags by API or in Hub . |
| `owner` | query | `string` | no | The API username for the account that processed the document. |
| `created__gt` | query | `string` | no | Return documents created after this date and time in UTC ISO 8601 format . |
| `created__lt` | query | `string` | no | Return documents created before this date and time in UTC ISO 8601 format . |
| `created__gte` | query | `string` | no | Return documents created beginning at this date and time in UTC ISO 8601 format . |
| `created__lte` | query | `string` | no | Return documents created on and before this date and time in UTC ISO 8601 format . |
| `updated__gt` | query | `string` | no | Return documents updated after this date and time in UTC ISO 8601 format . |
| `updated__lt` | query | `string` | no | Return documents updated before this date and time in UTC ISO 8601 format . |
| `updated__gte` | query | `string` | no | Return documents updated beginning at this date and time in UTC ISO 8601 format . |
| `updated__lte` | query | `string` | no | Return documents updated on and before this date and time in UTC ISO 8601 format . |
| `date__gt` | query | `string` | no | Return documents with the date field greater than this date and time in UTC ISO 8601 format . |
| `date__lt` | query | `string` | no | Return documents with the date field less than this date and time in UTC ISO 8601 format . |
| `date__gte` | query | `string` | no | Return documents with the date field greater than or equal to this date and time in UTC ISO 8601 format . |
| `date__lte` | query | `string` | no | Return documents with the date field less than or equal to this date and time in UTC ISO 8601 format . |
| `track_total_results` | query | `boolean` | no | Whether to always return accurate total_results and total_pages, true makes it slower. For increased performance, total results are not counted by default for search requests (with q parameter), and counted for list requests. |
