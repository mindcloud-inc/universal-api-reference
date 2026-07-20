# Upload Video with ZapCap

Uploads a video file to ZapCap.

## Endpoint

- **Method:** `POST`
- **Path:** `/videos`
- **Base URL:** `https://api.zapcap.ai`
- **Official documentation:** [Upload Video](https://platform.zapcap.ai/docs/api#tag/videos/post/videos)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Local MP4 or QuickTime file to upload to ZapCap. |
