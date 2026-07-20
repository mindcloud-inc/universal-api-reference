# Read Number Plates From Image with Platerecognizer

Reads vehicle number plates from an image with Plate Recognizer.

## Endpoint

- **Method:** `POST`
- **Path:** `/plate-reader/`
- **Base URL:** `https://api.platerecognizer.com/v1`
- **Official documentation:** [Read Number Plates From Image](https://guides.platerecognizer.com/docs/snapshot/api-reference/#read-number-plates-from-an-image)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `upload_url` | body | `string` | no | Public URL of the image to process. |
| `upload` | body | `file` | no | Image file bytes or a base64-encoded image. |
| `regions` | body | `string` | no | Comma-separated country or state codes to bias plate matching. |
| `camera_id` | body | `string` | no | Unique camera identifier. |
| `timestamp` | body | `date` | no | UTC ISO 8601 timestamp for the capture. |
| `mmc` | body | `boolean` | no | Set true to include make, model, orientation, color, and year when your plan includes this add-on. |
| `direction` | body | `boolean` | no | Set true to predict direction of travel. Requires mmc=true. |
| `config` | body | `object` | no | Additional engine configuration as JSON. |
