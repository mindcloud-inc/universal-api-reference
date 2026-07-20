# Update Video Group (V2) with Reka Vision

Updates an existing video group in Reka Vision.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/video-groups/:groupId`
- **Base URL:** `https://vision-agent.api.reka.ai`
- **Official documentation:** [Update Video Group (V2)](https://docs.reka.ai/vision/api-reference/v-2/update-video-group-v-2-video-groups-group-id-patch)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `group_id` | path | `string` | yes |
| `name` | body | `string` | no |
| `metadata` | body | `object` | no |
