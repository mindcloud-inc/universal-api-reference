# Quick Tag (V1) with Reka Vision

Creates metadata tags for short videos in Reka Vision.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/qa/quicktag`
- **Base URL:** `https://vision-agent.api.reka.ai`
- **Official documentation:** [Quick Tag (V1)](https://docs.reka.ai/vision/api-reference/v-1/quick-tag-v-1-qa-quicktag-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `video` | body | `file` | yes |
