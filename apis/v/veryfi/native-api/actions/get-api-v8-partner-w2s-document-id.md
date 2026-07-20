# Get a W-2 with Veryfi

Retrieves a W-2 from Veryfi.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v8/partner/w2s/:document_id`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Get a W-2](https://docs.veryfi.com/api/w2s/get-a-w-2/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | — |
| `bounding_boxes` | query | `boolean` | no | A field used to determine whether or not to return bounding_box and bounding_region for extracted fields in the Document response. |
| `confidence_details` | query | `boolean` | no | A field used to determine whether or not to return the score and ocr_score fields in the Document response. |
