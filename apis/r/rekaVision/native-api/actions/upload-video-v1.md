# Upload Video (V1) with Reka Vision

Uploads a video to Reka Vision.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/videos/upload`
- **Base URL:** `https://vision-agent.api.reka.ai`
- **Official documentation:** [Upload Video (V1)](https://docs.reka.ai/vision/api-reference/v-1/upload)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | no | — |
| `video_url` | body | `string` | no | — |
| `index` | body | `boolean` | yes | — |
| `enable_thumbnails` | body | `boolean` | no | — |
| `video_name` | body | `string` | no | — |
| `video_absolute_start_timestamp` | body | `string` | no | — |
| `config` | body | `string` | no | — |
| `person_indexing` | body | `boolean` | no | — |
| `persist_frames` | body | `boolean` | no | — |
| `caption_prompt` | body | `string` | no | — |
| `encode_chunks` | body | `boolean` | no | — |
| `caption_mode` | body | `list<string>` | no | Accepted values: `generic`, `security`, `tagging_ad_video`, `tte_1110`. |
| `group_id` | body | `string` | no | — |
| `chunking_config` | body | `string` | no | — |
