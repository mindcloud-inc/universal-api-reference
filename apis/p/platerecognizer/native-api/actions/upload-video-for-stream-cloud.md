# Upload Video For Stream Cloud with Platerecognizer

Uploads a video to Plate Recognizer Stream Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/stream/video-upload/`
- **Base URL:** `https://api.platerecognizer.com/v1`
- **Official documentation:** [Upload Video For Stream Cloud](https://guides.platerecognizer.com/docs/stream/cloud/video-upload-api/#http-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `upload_url` | body | `string` | no | Public URL of the video to process in Stream Cloud. |
| `regions` | body | `string` | no | Comma-separated country or state codes to bias plate matching. |
| `camera_id` | body | `string` | no | Unique camera identifier. |
| `mmc` | body | `boolean` | no | Set true to include make, model, orientation, and color when your license includes the add-on. |
