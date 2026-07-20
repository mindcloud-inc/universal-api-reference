# Read VIN From Image with Platerecognizer

Reads a VIN from an image with Plate Recognizer.

## Endpoint

- **Method:** `POST`
- **Path:** `/vin/reader/`
- **Base URL:** `https://api.platerecognizer.com/v1`
- **Official documentation:** [Read VIN From Image](https://guides.platerecognizer.com/docs/other-apps/vin-id/api-reference/#read-vin-from-an-image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `upload_url` | body | `string` | no | Public URL of the image to process. |
| `upload` | body | `file` | no | Image file bytes or a base64-encoded image. |
| `camera_id` | body | `string` | no | Unique camera identifier. |
| `timestamp` | body | `date` | no | UTC ISO 8601 timestamp for the capture. |
