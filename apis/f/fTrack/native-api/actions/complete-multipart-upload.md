# Complete Multipart Upload with FTrack

Completes a multipart upload in FTrack.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `{serverUrl}`
- **Official documentation:** [Complete Multipart Upload](https://developer.ftrack.com/api/operations/complete-multipart-upload-api-complete-multipart-upload-completemultipartupload-post/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `component_id` | body | `string` | yes | Component identifier whose multipart upload should be completed. |
| `upload_id` | body | `string` | yes | Upload identifier returned by the upload metadata call. |
| `parts[]` | body | `array<object>` | yes | Uploaded multipart parts. |
