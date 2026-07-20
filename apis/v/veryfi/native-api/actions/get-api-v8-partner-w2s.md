# Get W-2s with Veryfi

Retrieves W-2 documents from Veryfi.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v8/partner/w2s`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Get W-2s](https://docs.veryfi.com/api/w2s/get-w-2-s/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meta.tags[]` | query | `array<string>` | no | Return documents containing these tags. |
| `meta.external_id` | query | `string` | no | Return documents with this meta.external_id. |
| `created_date__gt` | query | `string` | no | Return documents created after this date and time in ISO 8601 format . |
| `created_date__lt` | query | `string` | no | Return documents created before this date and time in ISO 8601 format . |
| `created_date__gte` | query | `string` | no | Return documents created beginning at this date and time in ISO 8601 format . |
| `created_date__lte` | query | `string` | no | Return documents created on and before this date and time in ISO 8601 format . |
| `updated_date__gt` | query | `string` | no | Return documents updated after this date and time in ISO 8601 format . |
| `updated_date__lt` | query | `string` | no | Return documents updated before this date and time in ISO 8601 format . |
| `updated_date__gte` | query | `string` | no | Return documents updated beginning at this date and time in ISO 8601 format . |
| `updated_date__lte` | query | `string` | no | Return documents updated on and before this date and time in ISO 8601 format . |
| `page` | query | `number` | no | Default value: 1 The page number. The response is capped to maximum of 50 results per page. |
| `page_size` | query | `number` | no | Default value: 50 The number of Documents per page. |
| `bounding_boxes` | query | `boolean` | no | A field used to determine whether or not to return bounding_box and bounding_region for extracted fields in the Document response. |
| `confidence_details` | query | `boolean` | no | A field used to determine whether or not to return the score and ocr_score fields in the Document response. |
| `q` | query | `string` | no | Case sensitive. Return documents with this text or any extracted fields matching the value. Use asterisk for partial matches, e.g. q=Walmart* will return documents with either Walmart in ocr text or any extracted field containing Walmart. |
| `track_total_results` | query | `boolean` | no | Whether to always return accurate count of results, true makes it slower. |
