# Move Videos To Legacy Group with Reka AI

Updates legacy video group membership in Reka AI.

## Endpoint

- **Method:** `POST`
- **Path:** `https://vision-agent.api.reka.ai/v1/videos/group`
- **Base URL:** `https://api.reka.ai`
- **Official documentation:** [Move Videos To Legacy Group](https://docs.reka.ai/vision/api-reference/video-group/post-move-videos-to-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video_ids` | body | `string` | yes | Video IDs to move |
