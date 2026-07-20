# Get a W-8BEN-E with Veryfi

Retrieves a W-8BEN-E from Veryfi.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v8/partner/w-8ben-e/:document_id`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Get a W-8BEN-E](https://docs.veryfi.com/api/w-8ben-e/get-a-w-8-ben-e/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | — |
| `bounding_boxes` | query | `boolean` | no | A field used to determine whether or not to return bounding_box and bounding_region for extracted fields in the Document response. |
| `confidence_details` | query | `boolean` | no | A field used to determine whether or not to return the score and ocr_score fields in the Document response. |
