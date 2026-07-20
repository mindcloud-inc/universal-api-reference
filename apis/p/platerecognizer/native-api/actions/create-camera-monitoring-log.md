# Create Camera Monitoring Log with Platerecognizer

Creates a camera monitoring log in Plate Recognizer VisionAlert.

## Endpoint

- **Method:** `POST`
- **Path:** `/vision-alert/create-log/`
- **Base URL:** `https://api.platerecognizer.com/v1`
- **Official documentation:** [Create Camera Monitoring Log](https://guides.platerecognizer.com/docs/other-apps/vision-alert/api-reference/#create-camera-monitoring-log)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `camera_id` | body | `string` | yes | Unique camera identifier for the camera submitting the image. |
| `upload` | body | `file` | yes | Image file to analyze for camera issues. |
| `tag` | body | `string` | no | Tag to associate with the camera. |
