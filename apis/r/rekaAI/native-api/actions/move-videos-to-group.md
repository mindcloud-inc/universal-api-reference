# Move Videos To Group with Reka AI

Updates video group membership in Reka AI.

## Endpoint

- **Method:** `POST`
- **Path:** `https://vision-agent.api.reka.ai/v2/video-groups/:group_id/videos`
- **Base URL:** `https://api.reka.ai`
- **Official documentation:** [Move Videos To Group](https://docs.reka.ai/vision/api-reference/v-2/move-videos-to-group-v-2-video-groups-group-id-videos-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | path | `string` | yes | The destination video group identifier. |
| `video_ids` | body | `string` | yes | Video IDs to move |
