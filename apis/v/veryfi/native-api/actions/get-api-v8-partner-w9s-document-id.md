# Get a W-9 with Veryfi

Retrieves a W-9 from Veryfi.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v8/partner/w9s/:document_id`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Get a W-9](https://docs.veryfi.com/api/w9s/get-a-w-9/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | — |
| `bounding_boxes` | query | `boolean` | no | A field used to determine whether or not to return bounding_box and bounding_region for extracted fields in the Document response. |
| `confidence_details` | query | `boolean` | no | A field used to determine whether or not to return the score and ocr_score fields in the Document response. |
