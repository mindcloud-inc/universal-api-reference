# Get OCR Result with Mindee

Retrieves an OCR result from Mindee.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/products/ocr/results/:inference_id`
- **Base URL:** `https://api-v2.mindee.net`
- **Official documentation:** [Get OCR Result](https://docs.mindee.com/integrations/api-reference/ocr-models)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inference_id` | path | `string` | yes | UUID of the inference to retrieve. |
