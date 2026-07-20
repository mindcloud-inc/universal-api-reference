# Upload Video (V2) with Reka Vision

Uploads a video to Reka Vision without triggering indexing.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/videos`
- **Base URL:** `https://vision-agent.api.reka.ai`
- **Official documentation:** [Upload Video (V2)](https://docs.reka.ai/vision/api-reference/v-2/upload-video-v-2-videos-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | no |
| `video_url` | body | `string` | no |
| `video_name` | body | `string` | no |
| `group_id` | body | `string` | no |
| `description` | body | `string` | no |
