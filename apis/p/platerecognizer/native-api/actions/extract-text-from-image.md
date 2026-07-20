# Extract Text From Image with Platerecognizer

Extracts text from an image with Plate Recognizer OCR.

## Endpoint

- **Method:** `POST`
- **Path:** `/ocr/reader/`
- **Base URL:** `https://api.platerecognizer.com/v1`
- **Official documentation:** [Extract Text From Image](https://guides.platerecognizer.com/docs/other-apps/ocr/api-reference/#extract-text-from-an-image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `upload_url` | body | `string` | no | Public URL of the image to process. |
| `upload` | body | `file` | no | Image file bytes or a base64-encoded image. |
| `type` | body | `list<string>` | yes | Type of text to extract: vin, trailer_id, or odometer. Accepted values: `odometer`, `trailer_id`, `vin`. |
| `camera_id` | body | `string` | no | Unique camera identifier. |
| `timestamp` | body | `date` | no | UTC ISO 8601 timestamp for the capture. |
