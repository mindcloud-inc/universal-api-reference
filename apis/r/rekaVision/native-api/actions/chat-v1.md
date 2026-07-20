# Chat (V1) with Reka Vision

Retrieves video QA responses from Reka Vision.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/qa/chat`
- **Base URL:** `https://vision-agent.api.reka.ai`
- **Official documentation:** [Chat (V1)](https://docs.reka.ai/vision/api-reference/v-1/chat-v-1-qa-chat-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `user_id` | body | `string` | no |
| `video_id` | body | `string` | yes |
| `messages[]` | body | `array<object>` | no |
| `stream` | body | `boolean` | no |
| `apply_temporal_prefiltering` | body | `boolean` | no |
| `include_demo_videos` | body | `boolean` | no |
| `use_map_reduce_summarization` | body | `boolean` | no |
