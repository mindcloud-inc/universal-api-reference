# Complete Multipart Upload with ZapCap

Completes a multipart video upload in ZapCap.

## Endpoint

- **Method:** `POST`
- **Path:** `/videos/upload/complete`
- **Base URL:** `https://api.zapcap.ai`
- **Official documentation:** [Complete Multipart Upload](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/upload/complete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uploadId` | body | `string` | yes | Multipart upload session ID returned by Start Multipart Upload. |
| `videoId` | body | `string` | yes | Video ID returned by Start Multipart Upload. |
| `parts[]` | body | `array` | yes | Uploaded multipart parts with etag and partNumber values. |
