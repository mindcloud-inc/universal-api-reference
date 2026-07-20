# List Group Videos with Reka AI

Retrieves videos from a Reka AI video group.

## Endpoint

- **Method:** `GET`
- **Path:** `https://vision-agent.api.reka.ai/v2/video-groups/:group_id/videos`
- **Base URL:** `https://api.reka.ai`
- **Official documentation:** [List Group Videos](https://docs.reka.ai/vision/api-reference/v-2/list-group-videos-v-2-video-groups-group-id-videos-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | path | `string` | yes | The video group identifier whose videos to list. |
