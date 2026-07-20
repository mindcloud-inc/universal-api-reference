# Upload and Prepare Training Images with Apiframe

Uploads and prepares AI photo training images in Apiframe.

## Endpoint

- **Method:** `POST`
- **Path:** `/ai-photo-upload`
- **Base URL:** `https://api.apiframe.pro`
- **Official documentation:** [Upload and Prepare Training Images](https://docs.apiframe.ai/ai-photos/upload-and-prepare)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `images[]` | body | `array<string>` | yes |
| `ethnicity` | body | `string` | yes |
| `gender` | body | `string` | yes |
