# Indexed Tag (V1) with Reka Vision

Retrieves metadata tags for indexed videos in Reka Vision.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/qa/indexedtag`
- **Base URL:** `https://vision-agent.api.reka.ai`
- **Official documentation:** [Indexed Tag (V1)](https://docs.reka.ai/vision/api-reference/v-1/indexed-tag-v-1-qa-indexedtag-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `video_id` | body | `string` | yes |
