# Create Video Group (V2) with Reka Vision

Creates a new video group in Reka Vision.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/video-groups`
- **Base URL:** `https://vision-agent.api.reka.ai`
- **Official documentation:** [Create Video Group (V2)](https://docs.reka.ai/vision/api-reference/v-2/create-video-group-v-2-video-groups-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `metadata` | body | `object` | no |
