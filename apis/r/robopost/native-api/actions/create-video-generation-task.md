# Create Video Generation Task with Robopost

Creates a video generation task in Robopost.

## Endpoint

- **Method:** `POST`
- **Path:** `/video-tasks/{series_id}/generate`
- **Base URL:** `https://public-api.robopost.app/v1`
- **Official documentation:** [Create Video Generation Task](https://robopost.app/docs/robopost-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `series_id` | path | `string` | yes | The video series ID to generate a task for. |
