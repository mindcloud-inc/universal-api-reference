# Start OCR Job From URL with Mindee

Creates a new OCR job in Mindee from a URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/products/ocr/enqueue`
- **Base URL:** `https://api-v2.mindee.net`
- **Official documentation:** [Start OCR Job From URL](https://docs.mindee.com/integrations/api-reference/ocr-models)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model_id` | body | `string` | yes | Mindee model UUID to use for the OCR inference. |
| `url` | body | `string` | yes | Public HTTPS URL for the document to send to Mindee OCR. |
