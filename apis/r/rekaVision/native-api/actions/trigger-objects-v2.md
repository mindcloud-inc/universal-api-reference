# Trigger Objects (V2) with Reka Vision

Creates an object detection and tracking job in Reka Vision.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/videos/:videoId/features/objects`
- **Base URL:** `https://vision-agent.api.reka.ai`
- **Official documentation:** [Trigger Objects (V2)](https://docs.reka.ai/vision/api-reference/v-2/trigger-objects-v-2-videos-video-id-features-objects-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `video_id` | path | `string` | yes |
| `force` | body | `boolean` | no |
| `person_localization` | body | `object` | no |
| `person_localization.max_fps` | body | `number` | no |
| `person_localization.max_failed_frames` | body | `number` | no |
| `person_localization.num_photos_per_person` | body | `number` | no |
| `person_localization.max_objects_per_chunk` | body | `number` | no |
| `person_localization.conf` | body | `number` | no |
| `person_localization.iou` | body | `number` | no |
