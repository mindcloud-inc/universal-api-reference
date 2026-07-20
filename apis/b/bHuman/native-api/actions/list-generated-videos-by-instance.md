# List Generated Videos by Instance with BHuman

Retrieves generated videos for a video instance in BHuman.

## Endpoint

- **Method:** `GET`
- **Path:** `/ai_studio/generated_video_by_video_instance_id`
- **Base URL:** `https://studio.bhuman.ai/api`
- **Official documentation:** [List Generated Videos by Instance](https://github.com/bhuman-ai/public_api#api-endpoints)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video_instance_id` | query | `string` | yes | The video instance ID to look up generated videos for. |
