# Get a Business Card with Veryfi

Retrieves a business card from Veryfi.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v8/partner/business-cards/:document_id`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Get a Business Card](https://docs.veryfi.com/api/business-cards/get-a-business-card/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | — |
| `bounding_boxes` | query | `boolean` | no | A field used to determine whether or not to return bounding_box and bounding_region for extracted fields in the Document response. |
| `confidence_details` | query | `boolean` | no | A field used to determine whether or not to return the score and ocr_score fields in the Document response. |
