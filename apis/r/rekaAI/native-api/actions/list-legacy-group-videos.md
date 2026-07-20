# List Legacy Group Videos with Reka AI

Retrieves videos from a Reka AI legacy video group.

## Endpoint

- **Method:** `GET`
- **Path:** `https://vision-agent.api.reka.ai/v1/videos/groups/:group_id/videos`
- **Base URL:** `https://api.reka.ai`
- **Official documentation:** [List Legacy Group Videos](https://docs.reka.ai/vision/api-reference/video-groups/list-group-videos-v-1-videos-groups-group-id-videos-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | path | `string` | yes | The legacy video group identifier whose videos to list. |
