# Blur Plates And Faces In Image with Platerecognizer

Blurs plates and faces in an image with Plate Recognizer.

## Endpoint

- **Method:** `POST`
- **Path:** `https://blur.platerecognizer.com/v1/blur`
- **Base URL:** `https://api.platerecognizer.com/v1`
- **Official documentation:** [Blur Plates And Faces In Image](https://guides.platerecognizer.com/docs/other-apps/blur/api-reference/#blur-plates-and-faces-in-an-image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `upload_url` | body | `string` | no | Public URL of the image to blur. |
| `upload` | body | `file` | no | Image file to blur. |
| `plates` | body | `number` | no | Blur intensity for detected license plates. |
| `faces` | body | `number` | no | Blur intensity for detected faces. |
| `regions` | body | `string` | no | Comma-separated regions forwarded to Snapshot. |
| `camera_id` | body | `string` | no | Override configuration camera ID. |
